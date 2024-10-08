---
title: Remove-AzureADUserAppRoleAssignment
description: This article provides migration details from Remove-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADUserAppRoleAssignment

This article provides migration details from Remove-AzureADUserAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADUserAppRoleAssignment](/powershell/module/azuread/remove-azureaduserapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgUserAppRoleAssignment](/powershell/module/microsoft.graph.applications/remove-mguserapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgUserAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /users/{user-id}/appRoleAssignments/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-delete-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/user-delete-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|
|AppRoleAssignmentId|AppRoleAssignmentId|