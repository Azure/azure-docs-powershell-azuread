---
title: Get-AzureADDeletedApplication
description: This article provides migration details from Get-AzureADDeletedApplication command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDeletedApplication

This article provides migration details from Get-AzureADDeletedApplication command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDeletedApplication](/powershell/module/azuread/get-azureaddeletedapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryDeletedItem](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectorydeleteditem) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryDeletedItem))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: GET /directory/deletedItems | /directory/deletedItems/{directoryObject-id}

## Permissions

| Supported resource | Delegated (work or school account) | Delegated (personal Microsoft account) | Application |
|:-|:-|:-|:-|
| [administrativeUnit](../resources/administrativeunit) | AdministrativeUnit.Read.All | Not supported. | AdministrativeUnit.Read.All |
| [application](/graph/api/resources/application) | Application.Read.All | Not supported. | Application.Read.All |
| [group](/graph/api/resources/group) | Group.Read.All | Not supported. | Group.Read.All |
| [servicePrincipal](../resources/serviceprincipal) | Application.Read.All | Not supported. | Application.Read.All |
| [user](/graph/api/resources/user) | User.Read.All | Not supported. | User.Read.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DirectoryObjectId|
|All|All|
|Top|Top|
|Filter|Filter|