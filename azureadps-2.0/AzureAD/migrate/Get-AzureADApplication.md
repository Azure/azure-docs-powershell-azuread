---
title: Get-AzureADApplication
description: This article provides migration details from Get-AzureADApplication command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADApplication

This article provides migration details from Get-AzureADApplication command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADApplication](/powershell/module/azuread/get-azureadapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgApplication](/powershell/module/microsoft.graph.applications/get-mgapplication) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgApplication))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /applications/{applicationObjectId}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-get-permissions.md)]

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|Application.Read.All|Application.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|
|Delegated (personal Microsoft account)|Application.Read.All|Application.ReadWrite.All|
|Application|Application.Read.All|Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|

View more [details on permissions](/graph/api/application-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|Id|
|SearchString|NA|
|Top|Top|