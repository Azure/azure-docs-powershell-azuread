---
title: Get-AzureADMSGroup
description: This article provides migration details from Get-AzureADMSGroup command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSGroup

This article provides migration details from Get-AzureADMSGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSGroup](/powershell/module/azuread/get-azureadmsgroup)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroup](/powershell/module/microsoft.graph.groups/get-mggroup) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroup))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  GET /groups/{id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-get-permissions.md)]

View more [details on permissions](/graph/api/group-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|Id|
|SearchString|NA|
|Top|Top|