---
title: New-AzureADMSRoleAssignment
description: This article provides migration details from New-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/20/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSRoleAssignment

This article provides migration details from New-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSRoleAssignment](/powershell/module/azuread/new-azureadmsroleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgRoleManagementDirectoryRoleAssignment](/powershell/module/microsoft.graph.identity.governance/new-mgrolemanagementdirectoryroleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgRoleManagementDirectoryRoleAssignment))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint: POST /roleManagement/directory/roleAssignments

## Permissions

### For the directory (Microsoft Entra ID) provider
| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | RoleManagement.ReadWrite.Directory |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | RoleManagement.ReadWrite.Directory |

### For the entitlement management provider
|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EntitlementManagement.ReadWrite.All   |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | EntitlementManagement.ReadWrite.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|DirectoryScopeId|DirectoryScopeId|
|PrincipalId|PrincipalId|
|RoleDefinitionId|RoleDefinitionId|

> [!NOTE]
> You can specify the following properties when creating a **unifiedRoleAssignment**.

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|appScopeId|String|Required. Identifier of the app specific scope when the assignment scope is app specific. The scope of an assignment determines the set of resources for which the principal has been granted access. App scopes are scopes that are defined and understood by a resource application only. <br/><br/>For the entitlement management provider, use this property to specify a catalog, for example `/AccessPackageCatalog/beedadfe-01d5-4025-910b-84abb9369997`. <br/><br/> Either **appScopeId** or **directoryScopeId** must be specified.|
|directoryScopeId|String|Required. Identifier of the [directory object](/graph/api/resources/directoryobject) representing the scope of the assignment. The scope of an assignment determines the set of resources for which the principal has been granted access. Directory scopes are shared scopes stored in the directory that are understood by multiple applications, unlike app scopes that are defined and understood by a resource application only. <br/><br/> For the directory (Microsoft Entra ID) provider, this property supports the following formats: <li> `/` for tenant-wide scope <li> `/administrativeUnits/{administrativeunit-ID}` to scope to an administrative unit <li> `/{application-objectID}` to scope to a resource application <br/><br/> For entitlement management provider, `/` for tenant-wide scope. To scope to an access package catalog, use the **appScopeId** property. <br/><br/> Either **appScopeId** or **directoryScopeId** must be specified.|
|principalId|String|Required. Identifier of the principal to which the assignment is granted. |
|roleDefinitionId|String| Identifier of the unifiedRoleDefinition the assignment is for. Read-only. Supports `$filter` (`eq`, `in`). |
