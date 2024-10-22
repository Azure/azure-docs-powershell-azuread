---
title: Get-AzureADDirectoryRoleTemplate
description: This article provides migration details from Get-AzureADDirectoryRoleTemplate command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDirectoryRoleTemplate

This article provides migration details from Get-AzureADDirectoryRoleTemplate command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDirectoryRoleTemplate](/powershell/module/azuread/get-azureaddirectoryroletemplate)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryRoleTemplate](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectoryroletemplate) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryRoleTemplate))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: GET /directoryRoleTemplates | /directoryRoleTemplates/{directoryRoleTemplate-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryroletemplate-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DirectoryRoleTemplateId|