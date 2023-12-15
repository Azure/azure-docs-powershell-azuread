---
title: Remove-AzureADDevice
description: This article provides migration details from Remove-AzureADDevice command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADDevice

This article provides migration details from Remove-AzureADDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADDevice](/powershell/module/azuread/remove-azureaddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDevice](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions q=Remove-MgDevice))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /devices/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-delete-permissions.md)]

View more [details on permissions](/graph/api/device-delete#permissions).

The calling user must also be in one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json): *Global Administrator*, *Intune Administrator*, *Windows 365 Administrator*, or *Cloud Device Administrator*.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceId|