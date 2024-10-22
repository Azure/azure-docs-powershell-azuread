---
title: Get-AzureADServicePrincipalOAuth2PermissionGrant
description: This article provides migration details from Get-AzureADServicePrincipalOAuth2PermissionGrant command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADServicePrincipalOAuth2PermissionGrant

This article provides migration details from Get-AzureADServicePrincipalOAuth2PermissionGrant command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADServicePrincipalOAuth2PermissionGrant](/powershell/module/azuread/get-azureadapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipalOauth2PermissionGrant](/powershell/module/microsoft.graph.applications/get-mgserviceprincipaloauth2permissiongrant) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipalOauth2PermissionGrant))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /servicePrincipals/{servicePrincipal-id}/oauth2PermissionGrants

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-list-oauth2permissiongrants-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-list-oauth2permissiongrants#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|ServicePrincipalId|
|Top|Top|