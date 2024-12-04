---
services: active-directory
documentationcenter: ''
title: 'Working with administrative units'
ms.service: azure-active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 11/13/2024
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
ms.reviewer: stevemutungi
---

# Working with Administrative Units

In this article you learn how to use Azure AD PowerShell to work with Administrative Units. The article is made up of scripts that form a complete demo. The steps in this article help you to:

- Setup a demo environment for administrative units in your directory, 
- Create and populate administrative units 
- As a # Login as Privileged Role Administrator, assign roles to delegated admins 
- Sign in as a delegated admin to see the effects of the previous steps
- Finally, clean up all the objects we created in this demo.

## Demo scripts

### Step 1: Setup script
	
Run this script initially to create the users and admins used later in the demo.

```powershell
# Login as Privileged Role Administrator
Connect-AzureAD

### Create users we'll add as AU members later
$initialDomain = (Get-AzureADDomain)[0].Name
$passwordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile -ArgumentList "Windows2000", $false
for($i = 1; $i -le 2; $i++) {
    New-AzureADUser -UserPrincipalName "WestCoastUser$i@$initialDomain" -DisplayName "WestCoastUser$i" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastUser$i"
    New-AzureADUser -UserPrincipalName "EastCoastUser$i@$initialDomain" -DisplayName "EastCoastUser$i" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastUser$i"
}

### Create admins we'll assign later to manage the users in the AUs
New-AzureADUser -UserPrincipalName "WestCoastUserAdmin@$initialDomain" -DisplayName "WestCoastUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastUserAdmin"
New-AzureADUser -UserPrincipalName "WestCoastHelpdeskAdmin@$initialDomain" -DisplayName "WestCoastPasswordAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastPasswordAdmin"
New-AzureADUser -UserPrincipalName "EastCoastUserAdmin@$initialDomain" -DisplayName "EastCoastUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastUserAdmin"
New-AzureADUser -UserPrincipalName "EastCoastHelpdeskAdmin@$initialDomain" -DisplayName "EastCoastPasswordAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastPasswordAdmin"
New-AzureADUser -UserPrincipalName "MobileUserAdmin@$initialDomain" -DisplayName "MobileUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "MobileUserAdmin"

### Enable the Helpdesk Administrator Role using the templateId GUID for the role
Enable-AzureADDirectoryRole -RoleTemplateId "729827e3-9c14-49f7-bb1b-9608f156bbb8"

### Enable the User Account Administrator Role using the templateId GUID for the role
Enable-AzureADDirectoryRole -RoleTemplateId "fe930be7-5e62-47db-91af-98c3a49a38b1"

```

## Step 2: Create administrative units and assign roles

Run this script after the setup script to walk through the experience of creating and populating the AUs, and assigning the respective AU-scoped User Account and Helpdesk Admins.
```powershell
Connect-AzureAD

<# Simple Administrative Unit (AU) Demo

This demo walks through creating AUs for each region, adding members to those
AUs, and granting AU-scoped admin permissions. Our fictional company Contoso
has four users and two admins.  Contoso IT would like to segment admin
permissions into two regions, west coast and east coast. They will do this by
creating two AUs, West Coast and East Coast, then placing the corresponding
users into the respective AUs, and finally granting AU-scoped admin permissions
to the respective west coast and east coast admins.

#>

### List company information and users
Get-AzureADUser | ft DisplayName, UserPrincipalName

### Setup Administrative Units ######################################################
#Create West Coast AU
New-AzureADMSAdministrativeUnit -Description “West Coast region” -DisplayName “West Coast”
#Create East Coast AU
New-AzureADMSAdministrativeUnit -Description “East Coast region” -DisplayName “East Coast”

### Get the list of AUs
Get-AzureADMSAdministrativeUnit | ft DisplayName, Description

### Add West Coast AU member
$westCoastAU = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'West Coast'”
$initialDomain = (Get-AzureADDomain)[0].Name
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
$westCoastUser2 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser2@$InitialDomain'"
Add-AzureADMSAdministrativeUnitMember -Id $westCoastAU.Id -RefObjectId $westCoastUser1.ObjectId
Add-AzureADMSAdministrativeUnitMember -Id $westCoastAU.Id -RefObjectId $westCoastUser2.ObjectId
Get-AzureADMSAdministrativeUnitMember -Id $westCoastAU.Id

### Add East Coast AU member
$eastCoastAU = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'East Coast'”
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
$eastCoastUser2 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser2@$InitialDomain'"
Add-AzureADMSAdministrativeUnitMember -Id $eastCoastAU.Id -RefObjectId $eastCoastUser1.ObjectId
Add-AzureADMSAdministrativeUnitMember -Id $eastCoastAU.Id -RefObjectId $eastCoastUser2.ObjectId
Get-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId 
###################################################################################

### Delegate Admin Permissions Scoped to Administrative Units ######################
### Get list of available roles
$admins = Get-AzureADDirectoryRole
foreach($i in $admins) {
    if($i.DisplayName -eq "User Administrator") {
        $uaAdmin = $i
        }
    if($i.DisplayName -eq "Helpdesk Administrator") {
        $helpDeskAdmin = $i
        }
    }

### Add West Coast-scoped User Account Admin role member
$westCoastUA = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUserAdmin@$InitialDomain'"
$uaRoleMemberInfo = New-Object -TypeName Microsoft.Open.MSGraph.Model.MsRoleMemberInfo -Property @{Id =  $westCoastUA.Id }
Add-AzureADMSScopedRoleMembership -RoleId $uaAdmin.ObjectId -Id $westCoastAU.Id -RoleMemberInfo $uaRoleMemberInfo

### Add West Coast-scoped Helpdesk Admin role member
$westCoastHDA = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastHelpdeskAdmin@$InitialDomain'"
$hdaRoleMemberInfo = New-Object -TypeName Microsoft.Open.MSGraph.Model.MsRoleMemberInfo -Property @{Id =  $westCoastHDA.Id }
Add-AzureADMSScopedRoleMembership -RoleId $helpDeskAdmin.ObjectId -Id $westCoastHDA.Id -RoleMemberInfo $hdaRoleMemberInfo

### Get list of West coast AU Admins
Get-AzureADMSScopedRoleMembership -Id $westCoastAU.Id | fl *

### Add East Coast-scoped User Account Admin role member
$eastcoastua = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUserAdmin@$InitialDomain'"
$uaRoleMemberInfo = New-Object -TypeName Microsoft.Open.MSGraph.Model.MsRoleMemberInfo -Property @{Id =  $eastCoastUA.Id }
Add-AzureADMSScopedRoleMembership -RoleId $uaadmin.ObjectId -Id $eastCoastAU.Id -RoleMemberInfo $uaRoleMemberInfo

### Add East Coast-scoped Helpdesk Admin role member
$eastcoasthda = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastHelpdeskAdmin@$InitialDomain'"
$hdaRoleMemberInfo = New-Object -TypeName Microsoft.Open.MSGraph.Model.MsRoleMemberInfo -Property @{Id =  $eastCoastHDA.Id }
Add-AzureADScopedRoleMembership -RoleId $helpDeskAdmin.ObjectId -Id $eastCoastAU.Id -RoleMemberInfo $hdaRoleMemberInfo

### Get list of East coast AU Admins
Get-AzureADMSScopedRoleMembership -ObjectId $eastCoastAU.ObjectId | fl *
###################################################################################
```

### Step 3 : Sign in as User Administrator
	
Run this script to walk through the experience of an AU-scoped User Account Admin updating profile information, resetting passwords, and assigning licenses for users in their administrative unit.
```powershell
### Login as AU-scoped User Account Admin (WestCoastUserAdmin@<domain>, PS: Windows2000)
Connect-AzureAD

### Get list of West Coast AU members
$westCoastAU = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'West Coast'”
Get-AzureADMSAdministrativeUnitMember -Id $westCoastAU.Id

### Set department property (for example) for West Coast AU member.
$initialDomain = (Get-AzureADDomain)[0].Name
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
$westCoastUser1 | ft DisplayName, UserPrincipalName, department
$westCoastUser1.Department = 'West Coast'
Set-AzureADUser -ObjectId $westCoastUser1.ObjectId -Department $westCoastUser1.Department
Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'" | ft DisplayName, UserPrincipalName, department

### Reset password for West Cosat AU member
$password = ConvertTo-SecureString -String "123Password!" -AsPlainText -Force
Set-AzureADUserPassword -ObjectId $westCoastUser1.ObjectId -Password $password

### TODO: Example of assigning license for West Coast AU member

### Get list of East Coast AU members
$eastCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'East Coast'”
Get-AzureADMSAdministrativeUnitMember -Id $eastCoastAU.Id

### Attempt to set password for user in East Coast AU. All attempts to update users who are not members of West Coast AU should result in access denied.
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $eastCoastUser1.ObjectId -Password $password
```

### Sign in as Helpdesk Administrator

Run this script to walk through the experience of an AU-scoped Helpdesk Admin resetting passwords for users in their AU.

```powershell
#Login as East Coast Helpdesk Admin (EastCoastHelpdeskAdmin@<domain>, PS: Windows2000)
Connect-AzureAD

### Get list of East Coast AU members
$eastCoastAU = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'East Coast'”
Get-AzureADMSAdministrativeUnitMember -Id $eastCoastAU.Id | Get-AzureADUser

### Set password for user in East Coast AU
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $eastCoastUser1.ObjectId -Password $password

### Attempt to set password for user in West Coast AU. All attempts to update users who are not members of East Coast AU should result in access denied.
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $westCoastUser1.ObjectId -Password $password
```

## Cleanup

Run this script to delete the created users and administrative units.

```powershell
### Login as Privileged Role Administrator
Connect-AzureAD

### Cleanup demo

### Get roles used in demo
$admins = Get-AzureADDirectoryRole
foreach($i in $admins) {
    if($i.DisplayName -eq "User Administrator") {
        $uaadmin = $i
        }
    if($i.DisplayName -eq "Helpdesk Administrator") {
        $helpdeskadmin = $i
        }
    }
#####

## Delete all scoped role memberships used in demo
$adminunits = Get-AzureADMSAdministrativeUnit
foreach($adminunit in $adminunits) {
    $adminScopes = Get-AzureADMSScopedRoleMembership -Id $adminunit.ObjectId

    foreach($SRM in $adminScopes) {

        Remove-AzureADMSScopedRoleMembership -Id $adminunit.ObjectId -ScopedRoleMembershipId $SRM.Id
        }
    }
# Check all scoped role memberships were deleted
foreach($adminunit in $adminunits) {
    $adminScopes = Get-AzureADMSScopedRoleMembership -Id $adminunit.ObjectId
    }
####

## Delete demo Administrative Units
Get-AzureADAdministrativeUnit
$WestCoastAU = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'West Coast'”
foreach ($au in $WestCoastAU) {
    Remove-AzureADMSAdministrativeUnit –Id $au.Id
}
$eastcoastau = Get-AzureADMSAdministrativeUnit -Filter “displayname eq 'East Coast'”
foreach ($au in $eastcoastau) {
    Remove-AzureADMSAdministrativeUnit –Id $au.Id
}
Get-AzureADMSAdministrativeUnit
####

## Delete demo AU member users
Get-AzureADUser | ft DisplayName, UserPrincipalName
$initialDomain = (Get-AzureADDomain)[0].Name
for($i = 1; $i -le 2; $i++) {
    $westcoastuser = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser$i@$InitialDomain'"
    Remove-AzureADUser -ObjectId $westcoastuser.ObjectId
    $eastcoastuser = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser$i@$InitialDomain'"
    Remove-AzureADUser -ObjectId $eastcoastuser.ObjectId
}
Get-AzureADUser | ft DisplayName, UserPrincipalName
####

## Delete AU admin users
$westcoastua = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUserAdmin@$InitialDomain'"
Remove-AzureADUser -ObjectId $westcoastua.ObjectId
$westcoastha = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastHelpdeskAdmin@$InitialDomain'"
Remove-AzureADUser -ObjectId $westcoastha.ObjectId
$eastcoastua = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUserAdmin@$InitialDomain'"
Remove-AzureADUser -ObjectId $eastcoastua.ObjectId
$eastcoastha = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastHelpdeskAdmin@$InitialDomain'"
Remove-AzureADUser -ObjectId $eastcoastha.ObjectId
$mobileadmin = Get-AzureADUser -Filter "UserPrincipalName eq 'MobileUserAdmin@$InitialDomain'"
Remove-AzureADUser -ObjectId $mobileadmin.ObjectId
####

Get-AzureADUser | ft DisplayName, UserPrincipalName
Get-AzureADMSAdministrativeUnit

```

