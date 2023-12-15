---
title: Remove-AzureADDeviceRegisteredOwner
description: This article provides migration details from Remove-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADDeviceRegisteredOwner

This article provides migration details from Remove-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADDeviceRegisteredOwner](/powershell/module/azuread/remove-azureaddeviceregisteredowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDeviceRegisteredOwnerByRef](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdeviceregisteredownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgDeviceRegisteredOwnerByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /devices/{device-id}/registeredOwners/{directoryObject-id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-delete-registeredowners-permissions.md)]

View more [details on permissions](/graph/api/device-delete-registeredowners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceId|
|OwnerId|DirectoryObjectId|