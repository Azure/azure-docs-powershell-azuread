---
services: active-directory
documentationcenter: ''

ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
---

# Working with Administrative Units

Here are some demo scripts that you can use to learn how to use Azure AD PowerShell to work with Administrative Units. These scripts form a complete demo - You'll setup a demo environment for Administrative Units in your directory, see how to create and populate Administrative Units as a Global Admin and assign roles to delegated admins, and you'll see the effects of your actions when you sign in as a delegated admin, and finally there is a cleanup script to clean up all the object we created in this demo.

# Demo scripts

## Setup.ps1 
Run this script initially to create the users and admins used later in the demo.
```powershell
# Login as Global Administrator
Connect-AzureAD

#Create users we'll add as AU members later
$initialDomain = (Get-AzureADDomain)[0].Name
$passwordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile -ArgumentList "Windows2000", $false
for($i = 1; $i -le 2; $i++) {
    New-AzureADUser -UserPrincipalName "WestCoastUser$i@$initialDomain" -DisplayName "WestCoastUser$i" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastUser$i"
    New-AzureADUser -UserPrincipalName "EastCoastUser$i@$initialDomain" -DisplayName "EastCoastUser$i" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastUser$i"
}

#Create admins we'll assign later to manage the users in the AUs
New-AzureADUser -UserPrincipalName "WestCoastUserAdmin@$initialDomain" -DisplayName "WestCoastUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastUserAdmin"
New-AzureADUser -UserPrincipalName "WestCoastHelpdeskAdmin@$initialDomain" -DisplayName "WestCoastPasswordAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "WestCoastPasswordAdmin"
New-AzureADUser -UserPrincipalName "EastCoastUserAdmin@$initialDomain" -DisplayName "EastCoastUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastUserAdmin"
New-AzureADUser -UserPrincipalName "EastCoastHelpdeskAdmin@$initialDomain" -DisplayName "EastCoastPasswordAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "EastCoastPasswordAdmin"
New-AzureADUser -UserPrincipalName "MobileUserAdmin@$initialDomain" -DisplayName "MobileUserAdmin" -PasswordProfile $passwordProfile -UsageLocation "US" -AccountEnabled $true -MailNickName "MobileUserAdmin"

# Enable the Helpdesk Administrator Role
$haRole = "Helpdesk Administrator"
$role = Get-AzureADDirectoryRole | Where-Object {$_.displayName -eq $haRole}
if ($role -eq $null) {
    # Instantiate an instance of the role template
    $roleTemplate = Get-AzureADDirectoryRoleTemplate | Where-Object {$_.displayName -eq $haRole}
    Enable-AzureADDirectoryRole -RoleTemplateId $roleTemplate.ObjectId

    $role = Get-AzureADDirectoryRole | Where-Object {$_.displayName -eq $haRole}
}

# Enable the User Account Administrator Role
$uaaRole = "User Account Administrator"

$role = Get-AzureADDirectoryRole | Where-Object {$_.displayName -eq $uaaRole}
if ($role -eq $null) {
    # Instantiate an instance of the role template
    $roleTemplate = Get-AzureADDirectoryRoleTemplate | Where-Object {$_.displayName -eq $uaaRole}
    Enable-AzureADDirectoryRole -RoleTemplateId $roleTemplate.ObjectId

    $role = Get-AzureADDirectoryRole | Where-Object {$_.displayName -eq $uaaRole}
}
```

## Global Admin.ps1  
Run this script after the setup script to walk through the experience of a global admin creating and populating the AUs, and assigning the respective AU-scoped User Account and Helpdesk Admins.
```powershell
#Login as Global Administrator
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

#List company information and users
Get-AzureADUser | ft DisplayName, UserPrincipalName

## Setup Administrative Units ######################################################
#Create West Coast AU
New-AzureADAdministrativeUnit -Description “West Coast region” -DisplayName “West Coast”
#Create East Coast AU
New-AzureADAdministrativeUnit -Description “East Coast region” -DisplayName “East Coast”

#Get the list of AUs
Get-AzureADAdministrativeUnit | ft DisplayName, Description

#Add West Coast AU member
$westCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'West Coast'”
$initialDomain = (Get-AzureADDomain)[0].Name
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
$westCoastUser2 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser2@$InitialDomain'"
Add-AzureADAdministrativeUnitMember -ObjectId $westCoastAU.ObjectId -RefObjectId $westCoastUser1.ObjectId
Add-AzureADAdministrativeUnitMember -ObjectId $westCoastAU.ObjectId -RefObjectId $westCoastUser2.ObjectId
Get-AzureADAdministrativeUnitMember -ObjectId $westCoastAU.ObjectId | Get-AzureADUser

#Add East Coast AU member
$eastCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'East Coast'”
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
$eastCoastUser2 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser2@$InitialDomain'"
Add-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId -RefObjectId $eastCoastUser1.ObjectId
Add-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId -RefObjectId $eastCoastUser2.ObjectId
Get-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId | Get-AzureADUser
###################################################################################

## Delegate Admin Permissions Scoped to Administrative Units ######################
#Get list of available roles
$admins = Get-AzureADDirectoryRole
foreach($i in $admins) {
    if($i.DisplayName -eq "User Account Administrator") {
        $uaAdmin = $i
        }
    if($i.DisplayName -eq "Helpdesk Administrator") {
        $helpDeskAdmin = $i
        }
    }

#Add West Coast-scoped User Account Admin role member
$westCoastUA = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUserAdmin@$InitialDomain'"
$uaRoleMemberInfo = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo -Property @{ ObjectId =  $westCoastUA.ObjectId }
Add-AzureADScopedRoleMembership -RoleObjectId $uaAdmin.ObjectId -ObjectId $westCoastAU.ObjectId -RoleMemberInfo $uaRoleMemberInfo

#Add West Coast-scoped Helpdesk Admin role member
$westCoastHDA = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastHelpdeskAdmin@$InitialDomain'"
$hdaRoleMemberInfo = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo -Property @{ ObjectId =  $westCoastHDA.ObjectId }
Add-AzureADScopedRoleMembership -RoleObjectId $helpDeskAdmin.ObjectId -ObjectId $westCoastAU.ObjectId -RoleMemberInfo $hdaRoleMemberInfo

#Get list of West coast AU Admins
Get-AzureADScopedRoleMembership -ObjectId $westCoastAU.ObjectId | fl *

#Add East Coast-scoped User Account Admin role member
$eastcoastua = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUserAdmin@$InitialDomain'"
$uaRoleMemberInfo = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo -Property @{ ObjectId =  $eastCoastUA.ObjectId }
Add-AzureADScopedRoleMembership -RoleObjectId $uaadmin.ObjectId -ObjectId $eastCoastAU.ObjectId -RoleMemberInfo $uaRoleMemberInfo

#Add East Coast-scoped Helpdesk Admin role member
$eastcoasthda = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastHelpdeskAdmin@$InitialDomain'"
$hdaRoleMemberInfo = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo -Property @{ ObjectId =  $eastCoastHDA.ObjectId }
Add-AzureADScopedRoleMembership -RoleObjectId $helpDeskAdmin.ObjectId -ObjectId $eastCoastAU.ObjectId -RoleMemberInfo $hdaRoleMemberInfo

#Get list of East coast AU Admins
Get-AzureADScopedRoleMembership -ObjectId $eastCoastAU.ObjectId | fl *
###################################################################################
```

## AU UA Admin.ps1   
Run this script after the Global Admin script to walk through the experience of an AU-scoped User Account Admin updating profile information, resetting passwords, and assigning licenses for users in their AU.
```powershell
#Login as AU-scoped User Account Admin (WestCoastUserAdmin@<domain>, PS: Windows2000)
Connect-AzureAD

#Get list of West Coast AU members
$westCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'West Coast'”
Get-AzureADAdministrativeUnitMember -ObjectId $westCoastAU.ObjectId | Get-AzureADUser

#Set department property (for example) for West Coast AU member.
$initialDomain = (Get-AzureADDomain)[0].Name
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
$westCoastUser1 | ft DisplayName, UserPrincipalName, department
$westCoastUser1.Department = 'West Coast'
Set-AzureADUser -ObjectId $westCoastUser1.ObjectId -Department $westCoastUser1.Department
Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'" | ft DisplayName, UserPrincipalName, department

#Reset password for West Cosat AU member
$password = ConvertTo-SecureString -String "123Password!" -AsPlainText -Force
Set-AzureADUserPassword -ObjectId $westCoastUser1.ObjectId -Password $password

#TODO: Example of assigning license for West Coast AU member

#Get list of East Coast AU members
$eastCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'East Coast'”
Get-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId | Get-AzureADUser

#Attempt to set password for user in East Coast AU. All attempts to update users who are not members of West Coast AU should result in access denied.
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $eastCoastUser1.ObjectId -Password $password
```

## AU Helpdesk Admin.ps1 
Run this script after the Global Admin script to walk through the experience of an AU-scoped Helpdesk Admin resetting passwords for users in their AU.
```powershell
#Login as East Coast Helpdesk Admin (EastCoastHelpdeskAdmin@<domain>, PS: Windows2000)
Connect-AzureAD

#Get list of East Coast AU members
$eastCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'East Coast'”
Get-AzureADAdministrativeUnitMember -ObjectId $eastCoastAU.ObjectId | Get-AzureADUser

#Set password for user in East Coast AU
$eastCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'EastCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $eastCoastUser1.ObjectId -Password $password

#Attempt to set password for user in West Coast AU. All attempts to update users who are not members of East Coast AU should result in access denied.
$westCoastUser1 = Get-AzureADUser -Filter "UserPrincipalName eq 'WestCoastUser1@$InitialDomain'"
Set-AzureADUserPassword -ObjectId $westCoastUser1.ObjectId -Password $password
```

## Cleanup.ps1   
Run this script to delete the created users and AUs
```powershell
#Login as a Global Admin
Connect-AzureAD

#Cleanup demo

## Get roles used in demo
$admins = Get-AzureADDirectoryRole
foreach($i in $admins) {
    if($i.DisplayName -eq "User Account Administrator") {
        $uaadmin = $i
        }
    if($i.DisplayName -eq "Helpdesk Administrator") {
        $helpdeskadmin = $i
        }
    }
#####

## Delete all scoped role memberships used in demo
$adminunits = Get-AzureADAdministrativeUnit
foreach($adminunit in $adminunits) {
    $adminScopes = Get-AzureADScopedRoleMembership -ObjectId $adminunit.ObjectId
    foreach($SRM in $UaAdminScopes) {
        Remove-AzureADScopedRoleMembership -ObjectId $uaadmin.ObjectId -ScopedRoleMembershipId $SRM.Id
        Remove-AzureADScopedRoleMembership -ObjectId $helpdeskadmin.ObjectId -ScopedRoleMembershipId $SRM.Id
        }
    }
# Check all scoped role memberships were deleted
foreach($adminunit in $adminunits) {
    $adminScopes = Get-AzureADScopedRoleMembership -ObjectId $adminunit.ObjectId
    }
####

## Delete demo Administrative Units
Get-AzureADAdministrativeUnit
$WestCoastAU = Get-AzureADAdministrativeUnit -Filter “displayname eq 'West Coast'”
foreach ($au in $WestCoastAU) {
    Remove-AzureADAdministrativeUnit –ObjectId $au.ObjectId
}
$eastcoastau = Get-AzureADAdministrativeUnit -Filter “displayname eq 'East Coast'”
foreach ($au in $eastcoastau) {
    Remove-AzureADAdministrativeUnit –ObjectId $au.ObjectId
}
Get-AzureADAdministrativeUnit
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
Get-AzureADAdministrativeUnit
```

