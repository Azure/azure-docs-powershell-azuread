---
title: Get-AzureADDirectoryRole
description: This article provides migration details from Get-AzureADDirectoryRole command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDirectoryRole

This article provides migration details from Get-AzureADDirectoryRole command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDirectoryRole](/powershell/module/azuread/get-azureaddirectoryrole)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryRole](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectoryrole) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryRole))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /directoryRoles | /directoryRoles/{directoryRole-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryrole-get-permissions.md)]

View more [details on permissions](/graph/api/directoryrole-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Filter|Filter|
|ObjectId|DirectoryRoleId|