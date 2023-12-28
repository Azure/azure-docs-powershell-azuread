---
title: Add-AzureADMSLifecyclePolicyGroup
description: This article provides migration details from Add-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADMSLifecyclePolicyGroup

This article provides migration details from Add-AzureADMSLifecyclePolicyGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADMSLifecyclePolicyGroup](/powershell/module/azuread/add-azureadmslifecyclepolicygroup)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Add-MgGroupToLifecyclePolicy](/powershell/module/microsoft.graph.groups/add-mggrouptolifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Add-MgGroupToLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint: POST /groupLifecyclePolicies/{id}/addGroup

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-addgroup-permissions.md)]

View more [details on permissions](/graph/api/grouplifecyclepolicy-addgroup#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|GroupLifecyclePolicyId|
|GroupId|groupId|