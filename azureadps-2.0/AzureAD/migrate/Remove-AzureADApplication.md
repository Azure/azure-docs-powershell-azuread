---
title: Remove-AzureADApplication
description: This article provides migration details from Remove-AzureADApplication command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADApplication

This article provides migration details from Remove-AzureADApplication command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADApplication](/powershell/module/azuread/remove-azureadapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgApplication](/powershell/module/microsoft.graph.applications/remove-mgapplication) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgApplication))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /applications/{application-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-delete-permissions.md)]

View more [details on permissions](/graph/api/application-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|