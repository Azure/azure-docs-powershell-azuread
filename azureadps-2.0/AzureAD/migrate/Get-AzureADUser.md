---
title: Get-AzureADUser
description: This article provides migration details from Get-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUser

This article provides migration details from Get-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUser](/powershell/module/azuread/get-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUser](/powershell/module/microsoft.graph.users/get-mguser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET  /users/{user-id}

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|User.Read|User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|
|Delegated (personal Microsoft account)|User.Read|User.ReadWrite|
|Application|User.Read.All|User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|

View more [details on permissions](/graph/api/user-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|Id|
|SearchString|NA|
|Top|Top|