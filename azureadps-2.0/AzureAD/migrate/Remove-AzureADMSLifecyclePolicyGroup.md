---
title: Remove-AzureADMSLifecyclePolicyGroup
description: This article provides migration details from Remove-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSLifecyclePolicyGroup

This article provides migration details from Remove-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSLifecyclePolicyGroup](/powershell/module/azuread/remove-azureadmslifecyclepolicygroup)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgGroupFromLifecyclePolicy](/powershell/module/microsoft.graph.groups/remove-mggroupfromlifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgGroupFromLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  POST /groupLifecyclePolicies/{id}/removeGroup

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-removegroup-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|GroupLifecyclePolicyId|
|groupId|groupId|