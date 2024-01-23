---
title: Set-AzureADMSPermissionGrantPolicy
description: This article provides migration details from Set-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSPermissionGrantPolicy

This article provides migration details from Set-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSPermissionGrantPolicy](/powershell/module/azuread/set-azureadmspermissiongrantpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgPolicyPermissionGrantPolicy](/powershell/module/microsoft.graph.identity.signins/update-mgpolicypermissiongrantpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgPolicyPermissionGrantPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /policies/permissionGrantPolicies/{permissionGrantPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-update-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|
|Id|Id|