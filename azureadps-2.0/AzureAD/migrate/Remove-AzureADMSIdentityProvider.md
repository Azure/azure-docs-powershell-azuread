---
title: Remove-AzureADMSIdentityProvider
description: This article provides migration details from Remove-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSIdentityProvider

This article provides migration details from Remove-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSIdentityProvider](/powershell/module/azuread/remove-azureadmsidentityprovider)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgIdentityProvider](/powershell/module/microsoft.graph.identity.signins/remove-mgidentityprovider) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgIdentityProvider))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  DELETE /identity/identityProviders/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/identityproviderbase-delete-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|IdentityProviderBaseId|