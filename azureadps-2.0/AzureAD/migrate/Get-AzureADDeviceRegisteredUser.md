---
title: Get-AzureADDeviceRegisteredUser
description: This article provides migration details from Get-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDeviceRegisteredUser

This article provides migration details from Get-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDeviceRegisteredUser](/powershell/module/azuread/get-azureaddeviceregistereduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDeviceRegisteredUser](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdeviceregistereduser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDeviceRegisteredUser))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /devices/{device-id}/registeredUsers | /devices/{device-id}/registeredUsers/{directoryObject-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-list-registeredusers-permissions.md)]

View more [details on permissions](/graph/api/device-list-registeredusers#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|DeviceId|
|Top|Top|