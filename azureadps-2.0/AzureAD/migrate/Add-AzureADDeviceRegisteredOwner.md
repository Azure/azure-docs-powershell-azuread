---
title: Add-AzureADDeviceRegisteredOwner
description: This article provides migration details from Add-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADDeviceRegisteredOwner

This article provides migration details from Add-AzureADDeviceRegisteredOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADDeviceRegisteredOwner](/powershell/module/azuread/add-azureaddeviceregisteredowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDeviceRegisteredOwnerByRef](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdeviceregisteredownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDeviceRegisteredOwnerByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  POST /devices/{device-id}/registeredOwners/$ref

## Permissions

View more [details on permissions](/graph/api/device-post-registeredowners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceId|
|RefObjectId|OdataId|