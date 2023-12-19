---
title: Get-AzureADServicePrincipal
description: This article provides migration details from Get-AzureADServicePrincipal command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADServicePrincipal

This article provides migration details from Get-AzureADServicePrincipal command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADServicePrincipal](/powershell/module/azuread/get-azureadserviceprincipal)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipal](/powershell/module/microsoft.graph.applications/get-mgserviceprincipal) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipal))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /servicePrincipals | /servicePrincipals/{servicePrincipal-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-get-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|ServicePrincipalId|
|SearchString|NA|
|Top|Top|