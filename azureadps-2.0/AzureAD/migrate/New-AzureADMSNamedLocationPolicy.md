---
title: New-AzureADMSNamedLocationPolicy
description: This article provides migration details from New-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSNamedLocationPolicy

This article provides migration details from New-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSNamedLocationPolicy](/powershell/module/azuread/new-azureadmsnamedlocationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgIdentityConditionalAccessNamedLocation](/powershell/module/microsoft.graph.identity.signins/new-mgidentityconditionalaccessnamedlocation) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgIdentityConditionalAccessNamedLocation))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint: POST /identity/conditionalAccess/namedLocations

## Permissions

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All and Policy.ReadWrite.ConditionalAccess |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|CountriesAndRegions|CountriesAndRegions|
|DisplayName|DisplayName|
|Id|Id|
|IncludeUnknownCountriesAndRegions|IncludeUnknownCountriesAndRegions|
|IpRanges|IpRanges|
|IsTrusted|IsTrusted|
|OdataType|OdataType|