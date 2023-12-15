---
title: Get-AzureADDeviceRegisteredOwner
description: This article provides migration details from Get-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDeviceRegisteredOwner

This article provides migration details from Get-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDeviceRegisteredOwner](/powershell/module/azuread/get-azureaddeviceregisteredowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDeviceRegisteredOwner](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdeviceregisteredowner) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDeviceRegisteredOwner))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /devices/{device-id}/registeredOwners

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-list-registeredowners-permissions.md)]

View more [details on permissions](/graph/api/device-list-registeredowners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|DeviceId|
|Top|Top|