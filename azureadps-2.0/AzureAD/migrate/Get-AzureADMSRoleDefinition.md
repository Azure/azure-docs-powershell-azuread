---
title: Get-AzureADMSRoleDefinition
description: This article provides migration details from Get-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSRoleDefinition

This article provides migration details from Get-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSRoleDefinition](/powershell/module/azuread/get-azureadmsroledefinition)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgRoleManagementDirectoryRoleDefinition](/powershell/module/microsoft.graph.identity.governance/get-mgrolemanagementdirectoryroledefinition) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgRoleManagementDirectoryRoleDefinition))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint:  GET /roleManagement/directory/roleDefinitions | /roleManagement/directory/roleDefinitions/{unifiedRoleDefinition-id}

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
|Delegated (work or school account) |  EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All   |
|Delegated (personal Microsoft account) | Not supported.    |

View more [details on permissions](/graph/api/unifiedroledefinition-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|UnifiedRoleDefinitionId|
|SearchString|NA|
|Top|Top|