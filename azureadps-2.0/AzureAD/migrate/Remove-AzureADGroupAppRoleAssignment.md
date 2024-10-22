---
title: Remove-AzureADGroupAppRoleAssignment
description: This article provides migration details from Remove-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADGroupAppRoleAssignment

This article provides migration details from Remove-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADGroupAppRoleAssignment](/powershell/module/azuread/remove-azureadgroupapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgGroupAppRoleAssignment](/powershell/module/microsoft.graph.applications/remove-mggroupapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgGroupAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /groups/{group-id}/appRoleAssignments/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-delete-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/group-delete-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|AppRoleAssignmentId|AppRoleAssignmentId|