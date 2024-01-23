---
title: Remove-AzureADMSPermissionGrantConditionSet
description: This article provides migration details from Remove-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSPermissionGrantConditionSet

This article provides migration details from Remove-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSPermissionGrantConditionSet](/powershell/module/azuread/remove-azureadmspermissiongrantconditionset)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgPolicyPermissionGrantPolicyInclude](/powershell/module/microsoft.graph.identity.signins/remove-mgpolicypermissiongrantpolicyinclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgPolicyPermissionGrantPolicyInclude)); [Remove-MgPolicyPermissionGrantPolicyExclude](/powershell/module/microsoft.graph.identity.signins/remove-mgpolicypermissiongrantpolicyexclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgPolicyPermissionGrantPolicyExclude))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  DELETE /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/excludes/{permissionGrantConditionSet-id} | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/includes/{permissionGrantConditionSet-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-delete-excludes-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ConditionSetType|NA|
|Id|PermissionGrantConditionSetId|
|PolicyId|PermissionGrantPolicyId|