---
title: New-AzureADMSGroupLifecyclePolicy
description: This article provides migration details from New-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSGroupLifecyclePolicy

This article provides migration details from New-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSGroupLifecyclePolicy](/powershell/module/azuread/new-azureadmsgrouplifecyclepolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgGroupLifecyclePolicy](/powershell/module/microsoft.graph.groups/new-mggrouplifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgGroupLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint: POST /groupLifecyclePolicies

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-post-grouplifecyclepolicies-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AlternateNotificationEmails|AlternateNotificationEmails|
|GroupLifetimeInDays|GroupLifetimeInDays|
|ManagedGroupTypes|ManagedGroupTypes|