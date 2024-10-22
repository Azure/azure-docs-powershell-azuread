---
title: Get-AzureADDevice
description: This article provides migration details from Get-AzureADDevice command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDevice

This article provides migration details from Get-AzureADDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDevice](/powershell/module/azuread/get-azureaddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDevice](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDevice))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /devices | /devices/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-get-permissions.md)]

View more [details on permissions](/graph/api/device-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|DeviceId|
|SearchString|NA|
|Top|Top|