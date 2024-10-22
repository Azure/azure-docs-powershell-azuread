---
title: Remove-AzureADMSGroupLifecyclePolicy
description: This article provides migration details from Remove-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/17/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSGroupLifecyclePolicy

This article provides migration details from Remove-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSGroupLifecyclePolicy](/powershell/module/azuread/remove-azureadmsgrouplifecyclepolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgGroupLifecyclePolicy](/powershell/module/microsoft.graph.applications/remove-mggroupapproleassignment) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgGroupLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  DELETE /groupLifecyclePolicies/{groupLifecyclePolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-removegroup-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|Id|GroupLifecyclePolicyId|