---
title: Get-AzureADServiceAppRoleAssignedTo
description: This article provides migration details from Get-AzureADServiceAppRoleAssignedTo command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADServiceAppRoleAssignedTo

This article provides migration details from Get-AzureADServiceAppRoleAssignedTo command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADServiceAppRoleAssignedTo](/powershell/module/azuread/get-azureadserviceapproleassignedto)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipalAppRoleAssignedTo](/powershell/module/microsoft.graph.applications/get-mgserviceprincipalapproleassignedto) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipalAppRoleAssignedTo))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /servicePrincipals/{servicePrincipal-id}/appRoleAssignedTo | /servicePrincipals/{servicePrincipal-id}/appRoleAssignedTo/{appRoleAssignment-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-list-approleassignedto-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-list-approleassignedto#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|ServicePrincipalId|
|Top|Top|