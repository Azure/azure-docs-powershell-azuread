---
title: Set-AzureADMSIdentityProvider
description: This article provides migration details from Set-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSIdentityProvider

This article provides migration details from Set-AzureADMSIdentityProvider command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSIdentityProvider](/powershell/module/azuread/set-azureadmsidentityprovider)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgIdentityProvider](/powershell/module/microsoft.graph.groups/update-mggrouplifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgIdentityProvider))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /identity/identityProviders/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/identityproviderbase-update-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|IdentityProviderBaseId|