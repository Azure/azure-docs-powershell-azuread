---
title: Add-AzureADDeviceRegisteredUser
description: This article provides migration details from Add-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADDeviceRegisteredUser

This article provides migration details from Add-AzureADDeviceRegisteredUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADDeviceRegisteredUser](/powershell/module/azuread/add-azureaddeviceregistereduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDeviceRegisteredUserByRef](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdeviceregistereduserbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDeviceRegisteredUserByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  POST /devices/{device-id}/registeredUsers/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-post-registeredusers-permissions.md)]

View more [details on permissions](/graph/api/device-post-registeredusers#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceId|
|RefObjectId|OdataId|