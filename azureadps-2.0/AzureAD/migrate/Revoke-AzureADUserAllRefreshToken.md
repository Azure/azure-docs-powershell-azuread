---
title: Revoke-AzureADUserAllRefreshToken
description: This article provides migration details from Revoke-AzureADUserAllRefreshToken command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Revoke-AzureADUserAllRefreshToken

This article provides migration details from Revoke-AzureADUserAllRefreshToken command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Revoke-AzureADUserAllRefreshToken](/powershell/module/azuread/revoke-azureaduserallrefreshtoken)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Revoke-MgUserSignInSession](/powershell/module/microsoft.graph.users.actions/revoke-mgusersigninsession) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Revoke-MgUserSignInSession))
+ Graph Module: Microsoft.Graph.Users.Actions
+ Graph Endpoint:  POST /users/{id | userPrincipalName}/revokeSignInSessions

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-revokesigninsessions-permissions.md)]

View more [details on permissions](/graph/api/user-revokesigninsessions#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|