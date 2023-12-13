---
title: New-AzureADGroup
description: This article provides migration details from New-AzureADGroup command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/13/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADGroup

This article provides migration details from New-AzureADGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADGroup](/powershell/module/azuread/new-azureadgroup)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgGroup](/powershell/module/microsoft.graph.groups/new-mggroup) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgGroup))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint: POST /groups

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-post-groups-permissions.md)]

View more [details on permissions](/graph/api/group-post-groups#permissions).

For an app create a group with owners or members while it has the *Group.Create* permission, the app must have the privileges to read the object type that it wants to assign as the group owner or member. Therefore:
+ The app can assign itself as the group's owner or member.
+ To create the group with users as owners or members, the app must have at least the *User.Read.All* permission.
+ To create the group with other service principals as owners or members, the app must have at least the *Application.Read.All* permission.
+ To create the group with either users or service principals as owners or members, the app must have at least the *Directory.Read.All* permission.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|MailEnabled|MailEnabled|
|MailNickName|MailNickName|
|SecurityEnabled|SecurityEnabled|