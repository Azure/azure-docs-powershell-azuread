---
title: Remove-AzureADUser
description: This article provides migration details from Remove-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/14/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADUser

This article provides migration details from Remove-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADUser](/powershell/module/azuread/remove-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgUser](/powershell/module/microsoft.graph.users/remove-mguser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  DELETE /users/{id | userPrincipalName}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-delete-permissions.md)]

View more [details on permissions](/graph/api/user-delete#permissions).

The calling user must be assigned one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

- User Administrator
- Privileged Authentication Administrator
- Global Administrator

To delete users with privileged administrator roles in delegated scenarios, the app must be assigned the *Directory.AccessAsUser.All* delegated permission, and the calling user must have a higher privileged administrator role as indicated in [Who can perform sensitive actions](/graph/api/resources/users#who-can-perform-sensitive-actions).

In app-only scenarios, the *User.ReadWrite.All* application permission isn't enough privilege to delete users with privileged administrative roles. The app must be assigned a higher privileged administrator role as indicated in [Who can perform sensitive actions](/graph/api/resources/users#who-can-perform-sensitive-actions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|