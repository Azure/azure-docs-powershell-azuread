---
title: New-AzureADUserAppRoleAssignment
description: This article provides migration details from New-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADUserAppRoleAssignment

This article provides migration details from New-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADUserAppRoleAssignment](/powershell/module/azuread/new-azureaduserapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgUserAppRoleAssignment](/powershell/module/microsoft.graph.applications/new-mguserapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgUserAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /users/{user-id}/appRoleAssignments

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-post-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/user-post-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|Id|
|ObjectId|UserId|
|PrincipalId|PrincipalId|
|ResourceId|ResourceId|