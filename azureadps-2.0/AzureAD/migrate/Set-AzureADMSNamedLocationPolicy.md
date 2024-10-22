---
title: Set-AzureADMSNamedLocationPolicy
description: This article provides migration details from Set-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSNamedLocationPolicy

This article provides migration details from Set-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSNamedLocationPolicy](/powershell/module/azuread/set-azureadmsnamedlocationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgIdentityConditionalAccessNamedLocation](/powershell/module/microsoft.graph.identity.signins/update-mgidentityconditionalaccessnamedlocation) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgIdentityConditionalAccessNamedLocation))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /identity/conditionalAccess/namedLocations/{id}

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