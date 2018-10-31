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
