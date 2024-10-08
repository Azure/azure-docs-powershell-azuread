---
title: Get-AzureADMSRoleAssignment
description: This article provides migration details from Get-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSRoleAssignment

This article provides migration details from Get-AzureADMSRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSRoleAssignment](/powershell/module/azuread/get-azureadmsroleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgRoleManagementDirectoryRoleAssignment](/powershell/module/microsoft.graph.identity.governance/get-mgrolemanagementdirectoryroleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgRoleManagementDirectoryRoleAssignment))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint:  GET /roleManagement/directory/roleAssignments | /roleManagement/directory/roleAssignments/{unifiedRoleAssignment-id}

## Permissions

### For the directory (Microsoft Entra ID) provider
|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All |

### For the entitlement management provider
|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All  |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|Id|UnifiedRoleAssignmentId|
|SearchString||
|Top|Top|