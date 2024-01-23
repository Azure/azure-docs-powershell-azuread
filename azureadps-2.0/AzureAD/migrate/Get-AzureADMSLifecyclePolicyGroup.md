---
title: Get-AzureADMSLifecyclePolicyGroup
description: This article provides migration details from Get-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSLifecyclePolicyGroup

This article provides migration details from Get-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSLifecyclePolicyGroup](/powershell/module/azuread/get-azureadmslifecyclepolicygroup)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroupLifecyclePolicy](/powershell/module/microsoft.graph.groups/get-mggrouplifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroupLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  GET /groupLifecyclePolicies/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-get-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|GroupLifecyclePolicyId|