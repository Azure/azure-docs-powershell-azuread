---
title: Get-AzureADExtensionProperty
description: This article provides migration details from Get-AzureADExtensionProperty command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADExtensionProperty

This article provides migration details from Get-AzureADExtensionProperty command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADExtensionProperty](/powershell/module/azuread/get-azureadextensionproperty)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryObjectAvailableExtensionProperty](/powershell/module/microsoft.graph.directoryobjects/get-mgdirectoryobjectavailableextensionproperty) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryObjectAvailableExtensionProperty))
+ Graph Module: Microsoft.Graph.DirectoryObjects
+ Graph Endpoint: GET /directoryObjects/getAvailableExtensionProperties

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryobject-getavailableextensionproperties-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|IsSyncedFromOnPremises|IsSyncedFromOnPremises|