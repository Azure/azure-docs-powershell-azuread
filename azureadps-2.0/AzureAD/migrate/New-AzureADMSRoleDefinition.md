---
title: New-AzureADMSRoleDefinition
description: This article provides migration details from New-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSRoleDefinition

This article provides migration details from New-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSRoleDefinition](/powershell/module/azuread/new-azureadmsroledefinition)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgRoleManagementDirectoryRoleDefinition](/powershell/module/microsoft.graph.identity.governance/new-mgrolemanagementdirectoryroledefinition) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgRoleManagementDirectoryRoleDefinition))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /roleManagement/directory/roleDefinitions

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/rbacapplication-post-roledefinitions-permissions.md)]

View more [details on permissions](/graph/api/rbacapplication-post-roledefinitions#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|IsEnabled|IsEnabled|
|ResourceScopes|ResourceScopes|
|RolePermissions|RolePermissions|
|TemplateId|TemplateId|
|Version|Version|