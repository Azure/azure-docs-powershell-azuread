---
title: Remove-AzureADMSPermissionGrantPolicy
description: This article provides migration details from Remove-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSPermissionGrantPolicy

This article provides migration details from Remove-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSPermissionGrantPolicy](/powershell/module/azuread/remove-azureadmspermissiongrantpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgPolicyPermissionGrantPolicy](/powershell/module/microsoft.graph.identity.signins/remove-mgpolicypermissiongrantpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgPolicyPermissionGrantPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  DELETE /policies/permissionGrantPolicies/{permissionGrantPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-delete-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|PermissionGrantPolicyId|