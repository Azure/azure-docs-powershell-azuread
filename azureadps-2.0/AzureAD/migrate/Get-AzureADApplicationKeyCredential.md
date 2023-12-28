---
title: Get-AzureADApplicationKeyCredential
description: This article provides migration details from Get-AzureADApplicationKeyCredential command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADApplicationKeyCredential

This article provides migration details from Get-AzureADApplicationKeyCredential command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADApplicationKeyCredential](/powershell/module/azuread/get-azureadapplicationkeycredential)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgApplication](/powershell/module/microsoft.graph.applications/get-mgapplication) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgApplication))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: GET /applications/{applicationObjectId}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-get-permissions.md)]

View more [details on permissions](/graph/api/application-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|