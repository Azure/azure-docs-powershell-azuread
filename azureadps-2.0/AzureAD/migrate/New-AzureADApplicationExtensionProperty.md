---
title: New-AzureADApplicationExtensionProperty
description: This article provides migration details from New-AzureADApplicationExtensionProperty command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADApplicationExtensionProperty

This article provides migration details from New-AzureADApplicationExtensionProperty command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADApplicationExtensionProperty](/powershell/module/azuread/new-azureadapplicationextensionproperty)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgApplicationExtensionProperty](/powershell/module/microsoft.graph.applications/new-mgapplicationextensionproperty) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgApplicationExtensionProperty))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /applications/{application ObjectId}/extensionProperties

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-post-extensionproperty-permissions.md)]

View more [details on permissions](/graph/api/application-post-extensionproperty#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|