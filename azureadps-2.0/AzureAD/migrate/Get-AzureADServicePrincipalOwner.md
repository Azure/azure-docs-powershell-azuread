---
title: Get-AzureADServicePrincipalOwner
description: This article provides migration details from Get-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADServicePrincipalOwner

This article provides migration details from Get-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADServicePrincipalOwner](/powershell/module/azuread/get-azureadserviceprincipalowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipalOwner](/powershell/module/microsoft.graph.applications/get-mgserviceprincipalowner) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipalOwner))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /servicePrincipals/{servicePrincipal-id}/owners

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-list-owners-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-list-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|ServicePrincipalId|
|Top|Top|