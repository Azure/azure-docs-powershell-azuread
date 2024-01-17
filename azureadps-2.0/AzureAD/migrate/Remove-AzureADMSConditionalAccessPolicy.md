---
title: Remove-AzureADMSConditionalAccessPolicy
description: This article provides migration details from Remove-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSConditionalAccessPolicy

This article provides migration details from Remove-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSConditionalAccessPolicy](/powershell/module/azuread/remove-azureadmsconditionalaccesspolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgIdentityConditionalAccessPolicy](/powershell/module/microsoft.graph.identity.signins/remove-mgidentityconditionalaccesspolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgIdentityConditionalAccessPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  DELETE /identity/conditionalAccess/policies/{conditionalAccessPolicy-id}

## Permissions

|Permission type                        | Permissions (from least to most privileged)                    |
|:--------------------------------------|:---------------------------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|PolicyId|ConditionalAccessPolicyId|