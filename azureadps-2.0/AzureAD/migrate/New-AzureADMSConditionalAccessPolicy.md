---
title: New-AzureADMSConditionalAccessPolicy
description: This article provides migration details from New-AzureADMSConditionalAccessPolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 11/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSConditionalAccessPolicy

This article provides migration details from Add-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSConditionalAccessPolicy](/powershell/module/azuread/new-azureadmsconditionalaccesspolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgIdentityConditionalAccessPolicy](/powershell/module/microsoft.graph.identity.signins/new-mgidentityconditionalaccesspolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgIdentityConditionalAccessPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint: POST /identity/conditionalAccess/policies

## Permissions

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All, Policy.ReadWrite.ConditionalAccess and Application.Read.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All, Policy.ReadWrite.ConditionalAccess and Application.Read.All |

> [!NOTE]
> This method has a [known permissions issue](https://developer.microsoft.com/en-us/graph/known-issues/?search=13671) and may require consent to multiple permissions.

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Conditions|Conditions|
|DisplayName|DisplayName|
|GrantControls|GrantControls|
|Id|Id|
|SessionControls|SessionControls|
|State|State|