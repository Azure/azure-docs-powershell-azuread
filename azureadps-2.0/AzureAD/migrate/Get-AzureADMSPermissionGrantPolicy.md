---
title: Get-AzureADMSPermissionGrantPolicy
description: This article provides migration details from Get-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSPermissionGrantPolicy

This article provides migration details from Get-AzureADMSPermissionGrantPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSPermissionGrantPolicy](/powershell/module/azuread/get-azureadmspermissiongrantpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgPolicyPermissionGrantPolicy](/powershell/module/microsoft.graph.identity.signins/get-mgpolicypermissiongrantpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgPolicyPermissionGrantPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /policies/permissionGrantPolicies | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|PermissionGrantPolicyId|