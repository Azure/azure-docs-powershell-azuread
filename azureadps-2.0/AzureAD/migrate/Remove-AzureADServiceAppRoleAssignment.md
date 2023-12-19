---
title: Remove-AzureADServiceAppRoleAssignment
description: This article provides migration details from Remove-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADServiceAppRoleAssignment

This article provides migration details from Remove-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADServiceAppRoleAssignment](/powershell/module/azuread/remove-azureadserviceapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgServicePrincipalAppRoleAssignment](/powershell/module/microsoft.graph.applications/remove-mgserviceprincipalapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgServicePrincipalAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /servicePrincipals/{servicePrincipal-id}/appRoleAssignments/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-delete-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-delete-approleassignments#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ServicePrincipalId|
|AppRoleAssignmentId|AppRoleAssignmentId|