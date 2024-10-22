---
title: New-AzureADServiceAppRoleAssignment
description: This article provides migration details from New-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADServiceAppRoleAssignment

This article provides migration details from New-AzureADServiceAppRoleAssignment command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADServiceAppRoleAssignment](/powershell/module/azuread/new-azureadserviceapproleassignment)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgServicePrincipalAppRoleAssignment](/powershell/module/microsoft.graph.applications/new-mgserviceprincipalapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgServicePrincipalAppRoleAssignment))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /servicePrincipals/{servicePrincipal-id}/appRoleAssignments

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | AppRoleAssignment.ReadWrite.All and Application.Read.All, AppRoleAssignment.ReadWrite.All and Directory.Read.All |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | AppRoleAssignment.ReadWrite.All and Application.Read.All, AppRoleAssignment.ReadWrite.All and Directory.Read.All |

View more [details on permissions](/graph/api/serviceprincipal-post-approleassignments#permissions).

> [!NOTE]
> As a best practice, we recommend creating app role assignments through the [`appRoleAssignedTo` relationship of the _resource_ service principal](/graph/api/serviceprincipal-post-approleassignedto), instead of the `appRoleAssignments` relationship of the assigned user, group, or service principal.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|Id|
|ObjectId|ServicePrincipalId|
|PrincipalId|PrincipalId|
|ResourceId|ResourceId|