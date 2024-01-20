---
title: New-AzureADMSIdentityProvider
description: This article provides migration details from New-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSIdentityProvider

This article provides migration details from New-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSIdentityProvider](/powershell/module/azuread/new-azureadmsidentityprovider)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgIdentityProvider](/powershell/module/microsoft.graph.identity.signins/new-mgidentityprovider) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgIdentityProvider))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint: POST /identity/identityProviders

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/identitycontainer-post-identityproviders-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ClientId|ClientId|
|ClientSecret|ClientSecret|
|Type|identityProviderType|
|Name|displayName|