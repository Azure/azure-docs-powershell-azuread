---
title: Set-AzureADMSConditionalAccessPolicy
description: This article provides migration details from Set-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSConditionalAccessPolicy

This article provides migration details from Set-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSConditionalAccessPolicy](/powershell/module/azuread/set-azureadmsconditionalaccesspolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgIdentityConditionalAccessPolicy](/powershell/module/microsoft.graph.identity.signins/update-mgidentityconditionalaccesspolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgIdentityConditionalAccessPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /identity/conditionalAccess/policies/{conditionalAccessPolicy-id}

## Permissions

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All, Policy.ReadWrite.ConditionalAccess and Application.Read.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All, Policy.ReadWrite.ConditionalAccess and Application.Read.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Conditions|Conditions|
|DisplayName|DisplayName|
|GrantControls|GrantControls|
|Id|Id|
|SessionControls|SessionControls|
|State|State|