---
title: Get-AzureADUserManager
description: This article provides migration details from Get-AzureADUserManager command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserManager

This article provides migration details from Get-AzureADUserManager command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserManager](/powershell/module/azuread/get-azureadusermanager)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserManager](/powershell/module/microsoft.graph.users/get-mgusermanager) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserManager))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{user-id}/manager

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-manager-permissions.md)]

View more [details on permissions](/graph/api/user-list-manager#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|