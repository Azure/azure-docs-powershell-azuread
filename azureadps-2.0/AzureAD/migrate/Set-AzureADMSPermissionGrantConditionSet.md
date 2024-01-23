---
title: Set-AzureADMSPermissionGrantConditionSet
description: This article provides migration details from Set-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSPermissionGrantConditionSet

This article provides migration details from Set-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSPermissionGrantConditionSet](/powershell/module/azuread/set-azureadmspermissiongrantconditionset)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgPolicyPermissionGrantPolicyInclude](/powershell/module/microsoft.graph.identity.signins/update-mgpolicypermissiongrantpolicyinclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgPolicyPermissionGrantPolicyInclude)); [Update-MgPolicyPermissionGrantPolicyExclude](/powershell/module/microsoft.graph.identity.signins/update-mgpolicypermissiongrantpolicyexclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgPolicyPermissionGrantPolicyExclude))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/excludes/{permissionGrantConditionSet-id} | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/includes/{permissionGrantConditionSet-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-update-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ClientApplicationIds|ClientApplicationIds|
|ClientApplicationPublisherIds|ClientApplicationPublisherIds|
|ClientApplicationsFromVerifiedPublisherOnly|ClientApplicationsFromVerifiedPublisherOnly|
|ClientApplicationTenantIds|ClientApplicationTenantIds|
|ConditionSetType|NA|
|Id|Id|
|PermissionClassification|PermissionClassification|
|Permissions|Permissions|
|PermissionType|PermissionType|
|PolicyId|PermissionGrantPolicyId|
|ResourceApplication|ResourceApplication|