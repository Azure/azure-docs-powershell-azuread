---
title: Remove-AzureADDeviceRegisteredUser
description: This article provides migration details from Remove-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADDeviceRegisteredUser

This article provides migration details from Remove-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADDeviceRegisteredUser](/powershell/module/azuread/remove-azureaddeviceregistereduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDeviceRegisteredUserByRef](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdeviceregistereduserbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgDeviceRegisteredUserByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /devices/{device-id}/registeredUsers/{directoryObject-id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-delete-registeredusers-permissions.md)]

View more [details on permissions](/graph/api/device-delete-registeredusers#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceId|
|UserId|DirectoryObjectId|