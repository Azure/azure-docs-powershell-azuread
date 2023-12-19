---
title: Remove-AzureADServicePrincipal
description: This article provides migration details from Remove-AzureADServicePrincipal command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADServicePrincipal

This article provides migration details from Remove-AzureADServicePrincipal command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADServicePrincipal](/powershell/module/azuread/remove-azureadserviceprincipal)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgServicePrincipal](/powershell/module/microsoft.graph.applications/remove-mgserviceprincipal) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgServicePrincipal))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /servicePrincipals/{servicePrincipal-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-delete-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ServicePrincipalId|