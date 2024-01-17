---
title: Get-AzureADMSAuthorizationPolicy
description: This article provides migration details from Get-AzureADMSAuthorizationPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/17/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSAuthorizationPolicy

This article provides migration details from Get-AzureADMSAuthorizationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSAuthorizationPolicy](/powershell/module/azuread/get-azureadmsauthorizationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgPolicyAuthorizationPolicy](/powershell/module/microsoft.graph.identity.signins/get-mgpolicyauthorizationpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgPolicyAuthorizationPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /policies/authorizationPolicy | /policies/authorizationPolicy/{authorizationPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/authorizationpolicy-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|