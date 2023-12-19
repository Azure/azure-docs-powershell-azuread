---
title: Set-AzureADMSRoleDefinition
description: This article provides migration details from Set-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSRoleDefinition

This article provides migration details from Set-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSRoleDefinition](/powershell/module/azuread/set-azureadmsroledefinition)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgRoleManagementDirectoryRoleDefinition](/powershell/module/microsoft.graph.identity.governance/update-mgrolemanagementdirectoryroledefinition) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgRoleManagementDirectoryRoleDefinition))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint:  PATCH /roleManagement/directory/roleDefinitions/{unifiedRoleDefinition-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/unifiedroledefinition-update-permissions.md)]

View more [details on permissions](/graph/api/unifiedroledefinition-update#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|Id|Id|
|IsEnabled|IsEnabled|
|ResourceScopes|ResourceScopes|
|RolePermissions|RolePermissions|
|TemplateId|TemplateId|
|Version|Version|