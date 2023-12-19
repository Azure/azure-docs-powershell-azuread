---
title: Get-AzureADUserDirectReport
description: This article provides migration details from Get-AzureADUserDirectReport command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserDirectReport

This article provides migration details from Get-AzureADUserDirectReport command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserDirectReport](/powershell/module/azuread/get-azureaduserdirectreport)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserDirectReport](/powershell/module/microsoft.graph.users/get-mguserdirectreport) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserDirectReport))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{user-id}/directReports | /users/{user-id}/directReports/{directoryObject-id}

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | User.Read and User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All |
|Delegated (personal Microsoft account) | Not supported |
|Application | User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All |

View more [details on permissions](/graph/api/user-list-directreports#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|