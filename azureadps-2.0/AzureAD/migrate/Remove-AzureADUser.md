---
title: Remove-AzureADUser
description: This article provides migration details from Remove-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/14/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADUser

This article provides migration details from Remove-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADUser](/powershell/module/azuread/remove-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgUser](/powershell/module/microsoft.graph.users/remove-mguser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  DELETE /users/{id | userPrincipalName}

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|User.ReadWrite.All|Not available.|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|User.ReadWrite.All|Not available.|

View more [details on permissions](/graph/api/user-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|