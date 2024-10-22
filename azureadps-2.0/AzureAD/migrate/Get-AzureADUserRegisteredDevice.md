---
title: Get-AzureADUserRegisteredDevice
description: This article provides migration details from Get-AzureADUserRegisteredDevice command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserRegisteredDevice

This article provides migration details from Get-AzureADUserRegisteredDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserRegisteredDevice](/powershell/module/azuread/get-azureaduserregistereddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserRegisteredDevice](/powershell/module/microsoft.graph.users/get-mguserregistereddevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserRegisteredDevice))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{id | userPrincipalName}/registeredDevices

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-registereddevices-permissions.md)]

View more [details on permissions](/graph/api/user-list-registereddevices#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|UserId|
|Top|Top|