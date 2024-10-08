---
title: Enable-AzureADDirectoryRole
description: This article provides migration details from Enable-AzureADDirectoryRole command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Enable-AzureADDirectoryRole

This article provides migration details from Enable-AzureADDirectoryRole command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Enable-AzureADDirectoryRole](/powershell/module/azuread/enable-azureaddirectoryrole)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDirectoryRole](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdirectoryrole) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDirectoryRole))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  POST /directoryRoles

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryrole-post-directoryroles-permissions.md)]

View more [details on permissions](/graph/api/directoryrole-post-directoryroles#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|RoleTemplateId|roleTemplateId|
