---
title: Get-AzureADObjectByObjectId
description: This article provides migration details from Get-AzureADObjectByObjectId command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADObjectByObjectId

This article provides migration details from Get-AzureADObjectByObjectId command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADObjectByObjectId](/powershell/module/azuread/get-azureadobjectbyobjectid)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryObjectById](/powershell/module/microsoft.graph.directoryobjects/get-mgdirectoryobjectbyid) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryObjectById))
+ Graph Module: Microsoft.Graph.DirectoryObjects
+ Graph Endpoint:  POST /directoryObjects/getByIds

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryobject-getbyids-permissions.md)]

View more [details on permissions](/graph/api/directoryobject-getbyids#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectIds|ids, types e.g. "user","group","device"|