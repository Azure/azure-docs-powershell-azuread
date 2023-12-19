---
title: Get-AzureADServiceAppRoleAssignment
description: This article provides migration details from Get-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADServiceAppRoleAssignment

This article provides migration details from Get-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADServiceAppRoleAssignment](/powershell/module/azuread/get-azureadserviceapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipalAppRoleAssignment](/powershell/module/microsoft.graph.applications/get-mgserviceprincipalapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipalAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /servicePrincipals/{servicePrincipal-id}/appRoleAssignments

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-list-approleassignments-permissions.md)]

View more [details on permissions](/graph/api/approleassignment-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|ServicePrincipalId|
|Top|Top|