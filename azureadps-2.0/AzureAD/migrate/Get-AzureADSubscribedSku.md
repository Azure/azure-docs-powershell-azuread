---
title: Get-AzureADSubscribedSku
description: This article provides migration details from Get-AzureADSubscribedSku command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADSubscribedSku

This article provides migration details from Get-AzureADSubscribedSku command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADSubscribedSku](/powershell/module/azuread/get-azureadsubscribedsku)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgSubscribedSku](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgsubscribedsku) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgSubscribedSku))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /subscribedSkus | /subscribedSkus/{subscribedSku-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/subscribedsku-get-permissions.md)]

View more [details on permissions](/graph/api/subscribedsku-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|SubscribedSkuId|