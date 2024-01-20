---
title: New-AzureADMSPermissionGrantConditionSet
description: This article provides migration details from New-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSPermissionGrantConditionSet

This article provides migration details from New-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSPermissionGrantConditionSet](/powershell/module/azuread/new-azureadmsnamedlocationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgPolicyPermissionGrantPolicyInclude](/powershell/module/microsoft.graph.identity.signins/new-mgpolicypermissiongrantpolicyinclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgPolicyPermissionGrantPolicyInclude)); [New-MgPolicyPermissionGrantPolicyExclude](/powershell/module/microsoft.graph.identity.signins/new-mgpolicypermissiongrantpolicyexclude) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgPolicyPermissionGrantPolicyExclude))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint: POST /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/excludes | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/includes

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-post-excludes-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ClientApplicationIds|ClientApplicationIds|
|ClientApplicationPublisherIds|ClientApplicationPublisherIds|
|ClientApplicationsFromVerifiedPublisherOnly|ClientApplicationsFromVerifiedPublisherOnly|
|ClientApplicationTenantIds|ClientApplicationTenantIds|
|ConditionSetType|NA|
|PermissionClassification|PermissionClassification|
|Permissions|Permissions|
|PermissionType|PermissionType|
|PolicyId|PermissionGrantPolicyId|
|ResourceApplication|ResourceApplication|