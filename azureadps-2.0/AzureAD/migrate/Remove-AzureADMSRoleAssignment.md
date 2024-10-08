---
title: Remove-AzureADMSRoleAssignment
description: This article provides migration details from Remove-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSRoleAssignment

This article provides migration details from Remove-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSRoleAssignment](/powershell/module/azuread/remove-azureadmsroleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgRoleManagementDirectoryRoleAssignment](/powershell/module/microsoft.graph.identity.governance/remove-mgrolemanagementdirectoryroleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgRoleManagementDirectoryRoleAssignment))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint:  DELETE /roleManagement/directory/roleAssignments/{unifiedRoleAssignment-id}

## Permissions

### For the directory (Microsoft Entra ID) provider
| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | RoleManagement.ReadWrite.Directory |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | RoleManagement.ReadWrite.Directory |

### For the Entitlement management provider
|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EntitlementManagement.ReadWrite.All  |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | EntitlementManagement.ReadWrite.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|UnifiedRoleAssignmentId|