---
title: Remove-AzureADApplicationExtensionProperty
description: This article provides migration details from Remove-AzureADApplicationExtensionProperty command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADApplicationExtensionProperty

This article provides migration details from Remove-AzureADApplicationExtensionProperty command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADApplicationExtensionProperty](/powershell/module/azuread/remove-azureadapplicationextensionproperty)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgApplicationExtensionProperty](/powershell/module/microsoft.graph.applications/remove-mgapplicationextensionproperty) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgApplicationExtensionProperty))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: DELETE /applications/{application ObjectId}/extensionProperties/{extensionPropertyId}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/extensionproperty-delete-permissions.md)]

View more [details on permissions](/graph/api/extensionproperty-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ExtensionPropertyId|ExtensionPropertyId|
|ObjectId|ApplicationId|