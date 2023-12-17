---
title: Get-AzureADDirectoryRoleMember
description: This article provides migration details from Get-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDirectoryRoleMember

This article provides migration details from Get-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDirectoryRoleMember](/powershell/module/azuread/get-azureaddirectoryrolemember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryRoleMember](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectoryrolemember) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryRoleMember))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /directoryRoles/{directoryRole-id}/members

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryrole-list-members-permissions.md)]

View more [details on permissions](/graph/api/directoryrole-list-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DirectoryRoleId|