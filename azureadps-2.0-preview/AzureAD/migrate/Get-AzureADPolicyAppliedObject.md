---
title: Get-AzureADPolicyAppliedObject
description: This article provides migration details from Get-AzureADPolicyAppliedObject command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADPolicyAppliedObject

This article provides migration details from Get-AzureADPolicyAppliedObject command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADPolicyAppliedObject](/powershell/module/azuread/get-azureadpolicyappliedobject)
+ Azure AD Module: AzureADPreview
+ Microsoft Graph Command: [Get-MgBetaPolicyHomeRealmDiscoveryPolicyApplyTo](/powershell/module/microsoft.graph.beta.identity.signins/get-mgbetapolicyhomerealmdiscoverypolicyapplyto) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgBetaPolicyHomeRealmDiscoveryPolicyApplyTo))
+ Graph Module: Microsoft.Graph.Beta.Identity.SignIns
+ Graph Endpoint:  GET /servicePrincipals/{id}/homeRealmDiscoveryPolicies

## Permissions

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Policy.Read.All and Application.ReadWrite.All, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Policy.Read.All and Application.ReadWrite.OwnedBy, Policy.Read.All and Application.ReadWrite.All, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.OwnedBy, Policy.ReadWrite.ApplicationConfiguration and Application.ReadWrite.All |

View more [details on permissions](/graph/api/serviceprincipal-list-homerealmdiscoverypolicies#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|HomeRealmDiscoveryPolicyId|