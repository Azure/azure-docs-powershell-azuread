---
title: Remove-AzureADMSNamedLocationPolicy
description: This article provides migration details from Remove-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSNamedLocationPolicy

This article provides migration details from Remove-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSNamedLocationPolicy](/powershell/module/azuread/remove-azureadmsnamedlocationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgIdentityConditionalAccessNamedLocation](/powershell/module/microsoft.graph.identity.signins/remove-mgidentityconditionalaccessnamedlocation) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgIdentityConditionalAccessNamedLocation))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  DELETE /identity/conditionalAccess/namedLocations/{id}

## Permissions

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|PolicyId|NamedLocationId|