---
title: New-AzureADObjectSetting
description: This article provides migration details from New-AzureADObjectSetting command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADObjectSetting

This article provides migration details from New-AzureADObjectSetting command to Microsoft Graph PowerShell.

> [!IMPORTANT]
> This is a Beta command. The v1.0 version is also available as [New-MgGroupSetting](/powershell/module/microsoft.graph.groups/new-mggroupsetting). 

## Summary

+ Azure AD Command: [New-AzureADObjectSetting](/powershell/module/azuread/new-azureadobjectsetting)
+ Azure AD Module: AzureADPreview
+ Microsoft Graph Command: [New-MgBetaGroupSetting](/powershell/module/microsoft.graph.beta.groups/new-mgbetagroupsetting) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgBetaGroupSetting))
+ Graph Module: Microsoft.Graph.Beta.Groups
+ Graph Endpoint:  POST /groupSettings (Create a tenant-wide setting) | /groups/{id}/settings (Create a group-specific setting)

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-post-settings-permissions.md)]

View more [details on permissions](/graph/api/group-post-settings#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|DirectorySetting|NA|
|TargetObjectId|GroupId|
|TargetType|NA|