---
services: active-directory
documentationcenter: ''
title: 'List all applicaton roles'
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
description: Discover how to list all service principal application roles in your directory with our step-by-step guide on Microsoft Azure PowerShell.
---
# List all application role assignments for all service principals in your directory

If you want to list all service principals that have access to applications in your directory you can use the below script. The script will get all service principals in your directory, then for each service principal retrieve the service principal's application role assignments and will list the application roles that are assigned to the service principal.
```powershell
# Get all service principals, and for each one, get all the app role assignments, 
# resolving the app role ID to it's display name. 
Get-AzureADServicePrincipal | % {

  # Build a hash table of the service principal's app roles. The 0-Guid is
  # used in an app role assignment to indicate that the principal is assigned
  # to the default app role (or rather, no app role).
  $appRoles = @{ "$([Guid]::Empty.ToString())" = "(default)" }
  $_.AppRoles | % { $appRoles[$_.Id] = $_.DisplayName }

  # Get the app role assignments for this app, and add a field for the app role name
  Get-AzureADServiceAppRoleAssignment -ObjectId ($_.ObjectId) | Select ResourceDisplayName, PrincipalDisplayName,  Id | % {  $_ | Add-Member "AppRoleDisplayName" $appRoles[$_.Id] -Passthru
  }
}
```

> [!NOTE]
> If a particular application has more than 100 assignments above script would not return all the details.

#List all Users and Role assignments for a particular Service Principal in your directory. 

If you want to list all users and their role assignments for a specific Service Principal in your Azure Active Directory, you can use the below script. Since below script uses access token to call Graph API query you would need to have an App Registration with Directory.Read.All Permission to execute the script. In essence, this script provides a comprehensive list of all users and their role assignments for a specific Service Principal in your Azure Active Directory, exporting this information to a CSV file for easy viewing and analysis. This allows you to effectively manage and monitor the role assignments within your directory.

```powershell
# Define your tenant ID, client ID, and client secret
$tenantId = " <Your Azure AD Tenant ID>"
$clientId = " <Your Azure AD App Registration Client ID>"
$clientSecret = " <Your Azure AD App Registration Client Secret>"
# Define the resource and the scope
$resource = https://graph.microsoft.com
$scope = https://graph.microsoft.com/.default
# Define the token endpoint
$tokenEndpoint = https://login.microsoftonline.com/$tenantId/oauth2/v2.0/token
# Define the request body
$body = @{
    client_id     = $clientId
    scope         = $scope
    client_secret = $clientSecret
    grant_type    = "client_credentials"
}
# Send the request
$response = Invoke-RestMethod -Uri $tokenEndpoint -Method Post -Body $body
# Get the access token
$accessToken = $response.access_token
# Now you can use the access token in your requests to the Microsoft Graph API
# Define the batch size
$batchSize = 100
# Get the service principal; Replace the Name as needed.
$servicePrincipal = Get-MgServicePrincipal -Filter "displayName eq 'My Test App'"
# Get the app roles
$appRoles = $servicePrincipal.AppRoles
# Initialize the URL
$url = https://graph.microsoft.com/v1.0/servicePrincipals/$($servicePrincipal.Id)/appRoleAssignedTo
# Create an array to hold the results
$results = @()
# Loop until there are no more pages
while ($url) {
    # Send the request
    $response = Invoke-RestMethod -Uri $url -Headers @{Authorization = "Bearer $accessToken"}
    # Loop through each app role assignment
    foreach ($appRoleAssignment in $response.value) {
        # Get the user assigned to the app role
        $user = Get-MgUser -UserId $appRoleAssignment.principalId
        # Get the app role
        $appRole = $appRoles | Where-Object { $_.Id -eq $appRoleAssignment.appRoleId }
        # Add the user and app role information to the results array
        $results += New-Object PSObject -Property @{
            "User" = $user.DisplayName
            "App Role Name" = $appRole.DisplayName
            "App Role ID" = $appRole.Id
        }
    }
    # Get the next page URL
    $url = $response.'@odata.nextLink'
}
# Export the results to a CSV file
$results | Export-Csv -Path "AppRoleAssignments.csv" -NoTypeInformation
```
