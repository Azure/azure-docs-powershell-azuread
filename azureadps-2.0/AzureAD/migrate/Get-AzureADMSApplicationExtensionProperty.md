---
title: Get-AzureADMSApplicationExtensionProperty
description: This article provides migration details from Get-AzureADMSApplicationExtensionProperty command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSApplicationExtensionProperty

This article provides migration details from Get-AzureADMSApplicationExtensionProperty command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSApplicationExtensionProperty](/powershell/module/azuread/get-azureadmsapplicationextensionproperty)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgApplicationExtensionProperty](/powershell/module/microsoft.graph.applications/get-mgapplicationextensionproperty) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgApplicationExtensionProperty))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: GET /applications/{application-id}/extensionProperties | /applications/{application-id}/extensionProperties/{extensionProperty-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/extensionproperty-get-permissions.md)]

View more [details on permissions](/graph/api/extensionproperty-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|