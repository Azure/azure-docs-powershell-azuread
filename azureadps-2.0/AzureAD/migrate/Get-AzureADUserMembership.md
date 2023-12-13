---
title: Get-AzureADUserMembership
description: This article provides migration details from Get-AzureADUserMembership command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserMembership

This article provides migration details from Get-AzureADUserMembership command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserMembership](/powershell/module/azuread/get-azureadusermembership)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserMemberOf](/powershell/module/microsoft.graph.users/get-mgusermemberof) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserMemberOf))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{id | userPrincipalName}/memberOf

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-memberof-permissions.md)]

> **Note:** To list the members of a group with hidden membership, the Member.Read.Hidden permission is required.

View more [details on permissions](/graph/api/user-list-memberof#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|