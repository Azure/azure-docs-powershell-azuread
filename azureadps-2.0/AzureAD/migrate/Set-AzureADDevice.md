---
title: Set-AzureADDevice
description: This article provides migration details from Set-AzureADDevice command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADDevice

This article provides migration details from Set-AzureADDevice command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADDevice](/powershell/module/azuread/set-azureaddevice)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgDevice](/powershell/module/microsoft.graph.identity.directorymanagement/update-mgdevice) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgDevice))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  PATCH /devices/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/device-update-permissions.md)]

View more [details on permissions](/graph/api/device-update#permissions).

In application-only scenarios and for non-Windows devices, that is, where the **operatingSystem** property is not `Windows`, the app can update only the **extensionAttributes** property.

The calling user must also be in one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json): *Intune Administrator*. A calling user in the *Cloud Device Administrator* role can only enable or disable devices using this API and a user with the *Windows 365 Administrator* role can only update basic device properties.

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
|ObjectId|Id|