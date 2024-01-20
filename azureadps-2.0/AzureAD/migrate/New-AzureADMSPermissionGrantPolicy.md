---
title: New-AzureADMSPermissionGrantPolicy
description: This article provides migration details from New-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/20/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSPermissionGrantPolicy

This article provides migration details from New-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSPermissionGrantPolicy](/powershell/module/azuread/new-azureadmspermissiongrantpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgPolicyPermissionGrantPolicy](/powershell/module/microsoft.graph.identity.signins/new-mgpolicypermissiongrantpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgPolicyPermissionGrantPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint: POST /policies/permissionGrantPolicies

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-post-permissiongrantpolicies-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|Id|Id|