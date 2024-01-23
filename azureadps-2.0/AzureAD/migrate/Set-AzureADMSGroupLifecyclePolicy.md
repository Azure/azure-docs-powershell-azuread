---
title: Set-AzureADMSGroupLifecyclePolicy
description: This article provides migration details from Set-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSGroupLifecyclePolicy

This article provides migration details from Set-AzureADMSGroupLifecyclePolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSGroupLifecyclePolicy](/powershell/module/azuread/set-azureadmsgrouplifecyclepolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgGroupLifecyclePolicy](/powershell/module/microsoft.graph.groups/update-mggrouplifecyclepolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgGroupLifecyclePolicy))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  PATCH /groupLifecyclePolicies/{groupLifecyclePolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/grouplifecyclepolicy-update-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AlternateNotificationEmails|AlternateNotificationEmails|
|GroupLifetimeInDays|GroupLifetimeInDays|
|ManagedGroupTypes|ManagedGroupTypes|
|Id|Id|