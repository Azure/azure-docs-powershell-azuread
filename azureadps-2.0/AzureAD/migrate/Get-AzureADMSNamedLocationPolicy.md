---
title: Get-AzureADMSNamedLocationPolicy
description: This article provides migration details from Get-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSNamedLocationPolicy

This article provides migration details from Get-AzureADMSNamedLocationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSNamedLocationPolicy](/powershell/module/azuread/get-azureadmsnamedlocationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgIdentityConditionalAccessNamedLocation](/powershell/module/microsoft.graph.identity.signins/get-mgidentityconditionalaccessnamedlocation) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgIdentityConditionalAccessNamedLocation))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  GET /identity/conditionalAccess/namedLocations/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/countrynamedlocation-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|PolicyId|NamedLocationId|