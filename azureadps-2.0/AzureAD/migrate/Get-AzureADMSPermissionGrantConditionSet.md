---
title: Get-AzureADMSPermissionGrantConditionSet
description: This article provides migration details from Get-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSPermissionGrantConditionSet

This article provides migration details from Get-AzureADMSPermissionGrantConditionSet command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSPermissionGrantConditionSet](/powershell/module/azuread/get-azureadmspermissiongrantconditionset)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgPolicyPermissionGrantPolicyInclude](/powershell/module/microsoft.graph.identity.signins/get-mgidentityconditionalaccessnamedlocation) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgPolicyPermissionGrantPolicyInclude))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/excludes | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/excludes/{permissionGrantConditionSet-id} | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/includes | /policies/permissionGrantPolicies/{permissionGrantPolicy-id}/includes/{permissionGrantConditionSet-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/permissiongrantpolicy-list-includes-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ConditionSetType|NA|
|Id|PermissionGrantConditionSetId|
|PolicyId|PermissionGrantPolicyId|