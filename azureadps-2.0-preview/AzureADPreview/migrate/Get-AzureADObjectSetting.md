---
title: Get-AzureADObjectSetting
description: This article provides migration details from Get-AzureADObjectSetting command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADObjectSetting

This article provides migration details from Get-AzureADObjectSetting command to Microsoft Graph PowerShell.

> [!IMPORTANT]
> This is a Beta command. The v1.0 version is also available as [Get-MgGroupSetting](/powershell/module/Microsoft.Graph.Groups/Get-MgGroupSetting). 

## Summary

+ Azure AD Command: [Get-AzureADObjectSetting](/powershell/module/azuread/get-azureadobjectsetting)
+ Azure AD Module: AzureADPreview
+ Microsoft Graph Command: [Get-MgBetaGroupSetting](/powershell/module/Microsoft.Graph.Beta.Groups/Get-MgBetaGroupSetting) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgBetaGroupSetting))
+ Graph Module: Microsoft.Graph.Beta.Groups
+ Graph Endpoint:  GET /groupSettings/{groupSettingId} | /groups/{groupId}/settings/{groupSettingId}

## Permissions

### List tenant-wide settings

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Directory.Read.All, Directory.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | Directory.Read.All, Directory.ReadWrite.All |

### List group-specific settings

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Group.Read.All, Group.ReadWrite.All         |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | Group.Read.All, Group.ReadWrite.All         |

View more [details on permissions](/graph/api/groupsetting-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|NA|
|Id|NA|
|TargetObjectId|GroupId|
|TargetType|NA|
|Top|NA|