---
title: Get-AzureADMSConditionalAccessPolicy
description: This article provides migration details from Get-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSConditionalAccessPolicy

This article provides migration details from Get-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSConditionalAccessPolicy](/powershell/module/azuread/get-azureadmsconditionalaccesspolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgIdentityConditionalAccessPolicy](/powershell/module/microsoft.graph.identity.signins/get-mgidentityconditionalaccesspolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgIdentityConditionalAccessPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /identity/conditionalAccess/policies | /identity/conditionalAccess/policies/{conditionalAccessPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/conditionalaccesspolicy-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|PolicyId|ConditionalAccessPolicyId|