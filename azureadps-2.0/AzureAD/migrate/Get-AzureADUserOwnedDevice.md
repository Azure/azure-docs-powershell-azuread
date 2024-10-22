---
title: Get-AzureADUserOwnedDevice
description: This article provides migration details from Get-AzureADUserOwnedDevice command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserOwnedDevice

This article provides migration details from Get-AzureADUserOwnedDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserOwnedDevice](/powershell/module/azuread/get-azureaduserowneddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserOwnedDevice](/powershell/module/microsoft.graph.users/get-mguserowneddevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserOwnedDevice))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{id | userPrincipalName}/ownedDevices

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-owneddevices-permissions.md)]

View more [details on permissions](/graph/api/user-list-owneddevices#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|