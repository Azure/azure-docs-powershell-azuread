---
title: New-AzureADDevice
description: This article provides migration details from New-AzureADDevice command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/13/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADDevice

This article provides migration details from New-AzureADDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADDevice](/powershell/module/azuread/new-azureaddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDevice](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDevice))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: POST /devices

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-post-devices-permissions.md)]

View more [details on permissions](/graph/api/device-post-devices#permissions).

The calling user must also be in one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json): *Intune Administrator*, or *Windows 365 Administrator*.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AccountEnabled|AccountEnabled|
|AlternativeSecurityIds|AlternativeSecurityIds|
|ApproximateLastLogonTimeStamp|NA|
|DeviceId|DeviceId|
|DeviceMetadata|DeviceMetadata|
|DeviceObjectVersion|NA|
|DeviceOSType|NA|
|DeviceOSVersion|NA|
|DevicePhysicalIds|NA|
|DeviceTrustType|NA|
|IsCompliant|IsCompliant|
|DisplayName|DisplayName|
|IsManaged|IsManaged|
|ProfileType|ProfileType|
|SystemLabels|SystemLabels|