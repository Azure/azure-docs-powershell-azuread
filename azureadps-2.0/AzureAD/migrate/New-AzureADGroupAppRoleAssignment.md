---
title: New-AzureADGroupAppRoleAssignment
description: This article provides migration details from New-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADGroupAppRoleAssignment

This article provides migration details from New-AzureADGroupAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADGroupAppRoleAssignment](/powershell/module/azuread/new-azureadgroupapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgGroupAppRoleAssignment](/powershell/module/microsoft.graph.applications/new-mggroupapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgGroupAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /groups/{groupId}/appRoleAssignments

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-post-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/group-post-approleassignments#permissions).

> [!NOTE]
> As a best practice, we recommend creating app role assignments through the [`appRoleAssignedTo` relationship of the _resource_ service principal](serviceprincipal-post-approleassignedto.md), instead of the `appRoleAssignments` relationship of the assigned user, group, or service principal.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|Id|
|ObjectId|GroupId|
|PrincipalId|PrincipalId|
|ResourceId|ResourceId|