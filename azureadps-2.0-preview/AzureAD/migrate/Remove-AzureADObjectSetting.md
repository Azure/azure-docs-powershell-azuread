---
title: Remove-AzureADObjectSetting
description: This article provides migration details from Remove-AzureADObjectSetting command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADObjectSetting

This article provides migration details from Remove-AzureADObjectSetting command to Microsoft Graph PowerShell.

> [!IMPORTANT]
> This is a Beta command. The v1.0 version is also available as [Remove-MgGroupSetting](/powershell/module/Microsoft.Graph.Groups/Remove-MgGroupSetting). 

## Summary

+ Azure AD Command: [Remove-AzureADObjectSetting](/powershell/module/azuread/remove-azureadobjectsetting)
+ Azure AD Module: AzureADPreview
+ Microsoft Graph Command: [Remove-MgBetaGroupSetting](/powershell/module/microsoft.graph.beta.groups/remove-mgbetagroupsetting) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgBetaGroupSetting))
+ Graph Module: Microsoft.Graph.Beta.Groups
+ Graph Endpoint:  DELETE /groupSettings/{groupSettingId} (Delete a tenant-wide setting) | /groups/{groupId}/settings/{groupSettingId} (Delete a group-specific setting)

## Permissions

### For all settings except the Consent Policy Settings object

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Directory.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Directory.ReadWrite.All |

### For the Consent Policy Settings object

The following permissions are required to update the "Consent Policy Settings" **directorySetting** object.

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Policy.ReadWrite.Authorization    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Policy.ReadWrite.Authorization |

View more [details on permissions](/graph/api/groupsetting-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|NA|
|TargetObjectId|GroupId|
|TargetType|NA|