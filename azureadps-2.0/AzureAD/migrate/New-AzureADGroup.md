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

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|Group.ReadWrite.All|Directory.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|Group.Create|Directory.ReadWrite.All, Group.ReadWrite.All|

View more [details on permissions](/graph/api/group-post-groups#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|MailEnabled|MailEnabled|
|MailNickName|MailNickName|
|SecurityEnabled|SecurityEnabled|