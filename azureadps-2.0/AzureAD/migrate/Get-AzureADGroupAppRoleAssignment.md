---
title: Get-AzureADGroupAppRoleAssignment
description: This article provides migration details from Get-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADGroupAppRoleAssignment

This article provides migration details from Get-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADGroupAppRoleAssignment](/powershell/module/azuread/get-azureadgroupapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroupAppRoleAssignment](/powershell/module/microsoft.graph.applications/get-mggroupapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroupAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /groups/{group-id}/appRoleAssignments/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-list-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/group-list-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|