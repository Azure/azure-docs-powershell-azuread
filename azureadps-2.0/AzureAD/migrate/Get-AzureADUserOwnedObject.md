---
title: Get-AzureADUserOwnedObject
description: This article provides migration details from Get-AzureADUserOwnedObject command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserOwnedObject

This article provides migration details from Get-AzureADUserOwnedObject command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserOwnedObject](/powershell/module/azuread/get-azureaduserownedobject)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserOwnedObject](/powershell/module/microsoft.graph.users/get-mguserownedobject) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserOwnedObject))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{user-id}/ownedObjects | /users/{user-id}/ownedObjects/{directoryObject-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-ownedobjects-permissions.md)]

View more [details on permissions](/graph/api/user-list-ownedobjects#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|UserId|
|Top|Top|