---
title: Set-AzureADUserLicense
description: This article provides migration details from Set-AzureADUserLicense command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 11/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADUserLicense

This article provides migration details from Set-AzureADUserLicense command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADUserLicense](/powershell/module/azuread/set-azureaduserlicense)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Set-MgUserLicense](/powershell/module/microsoft.graph.users.actions/set-mguserlicense) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Set-MgUserLicense))
+ Graph Module: Microsoft.Graph.Users.Actions
+ Graph Endpoint:  POST /users/{id | userPrincipalName}/assignLicense

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-assignlicense-permissions.md)]

View more [details on permissions](/graph/api/user-assignlicense#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AssignedLicenses|AssignedLicenses|
|ObjectId|UserId|