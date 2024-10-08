---
title: Get-AzureADUserCreatedObject
description: This article provides migration details from Get-AzureADUserCreatedObject command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserCreatedObject

This article provides migration details from Get-AzureADUserCreatedObject command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserCreatedObject](/powershell/module/azuread/get-azureadusercreatedobject)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserCreatedObject](/powershell/module/microsoft.graph.users/get-mgusercreatedobject) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserCreatedObject))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{user-id}/createdObjects | /users/{user-id}/createdObjects/{directoryObject-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-createdobjects-permissions.md)]

View more [details on permissions](/graph/api/user-list-createdobjects#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|UserId|
|Top|Top|