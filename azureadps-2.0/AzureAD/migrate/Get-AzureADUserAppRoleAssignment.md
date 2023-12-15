---
title: Get-AzureADUserAppRoleAssignment
description: This article provides migration details from Get-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserAppRoleAssignment

This article provides migration details from Get-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserAppRoleAssignment](/powershell/module/azuread/get-azureaduserapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserAppRoleAssignment](/powershell/module/microsoft.graph.applications/get-mguserapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /users/{user-id}/appRoleAssignments | /users/{user-id}/appRoleAssignments/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/user-list-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|