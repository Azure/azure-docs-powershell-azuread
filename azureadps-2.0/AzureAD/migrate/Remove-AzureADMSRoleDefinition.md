---
title: Remove-AzureADMSRoleDefinition
description: This article provides migration details from Remove-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSRoleDefinition

This article provides migration details from Remove-AzureADMSRoleDefinition command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSRoleDefinition](/powershell/module/azuread/remove-azureadmsroledefinition)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgRoleManagementDirectoryRoleDefinition](/powershell/module/microsoft.graph.identity.governance/remove-mgrolemanagementdirectoryroledefinition) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgRoleManagementDirectoryRoleDefinition))
+ Graph Module: Microsoft.Graph.Identity.Governance
+ Graph Endpoint:  DELETE /roleManagement/directory/roleDefinitions/{unifiedRoleDefinition-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/unifiedroledefinition-delete-permissions.md)]

View more [details on permissions](/graph/api/unifiedroledefinition-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UnifiedRoleDefinitionId|