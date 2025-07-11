---
title: Set-AzureADObjectSetting
description: This article provides migration details from Set-AzureADObjectSetting command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADObjectSetting

This article provides migration details from Set-AzureADObjectSetting command to Microsoft Graph PowerShell.

> [!IMPORTANT]
> This is a Beta command. The v1.0 version is also available as [Update-MgGroupSetting](/powershell/module/Microsoft.Graph.Groups/Update-MgGroupSetting). 

## Summary

+ Azure AD Command: [Set-AzureADObjectSetting](/powershell/module/azuread/set-azureadobjectsetting)
+ Azure AD Module: AzureADPreview
+ Microsoft Graph Command: [Update-MgBetaGroupSetting](/powershell/module/microsoft.graph.beta.groups/update-mgbetagroupsetting) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgBetaGroupSetting))
+ Graph Module: Microsoft.Graph.Beta.Groups
+ Graph Endpoint: PATCH /groupSettings/{groupSettingId} (Update a tenant-wide setting) | PATCH /groups/{groupId}/settings/{groupSettingId} (Update a group-specific setting)

## Permissions

### List tenant-wide settings

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

View more [details on permissions](/graph/api/groupsetting-update#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|NA|
|TargetObjectId|GroupId|
|TargetType|NA|
|DirectorySetting|DirectorySettingId|