---
title: Get-AzureADMSIdentityProvider
description: This article provides migration details from Get-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSIdentityProvider

This article provides migration details from Get-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSIdentityProvider](/powershell/module/azuread/get-azureadmsidentityprovider)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgIdentityProvider](/powershell/module/microsoft.graph.identity.signins/get-mgidentityprovider) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgIdentityProvider))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /identity/identityProviders/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/identityproviderbase-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|IdentityProviderBaseId|