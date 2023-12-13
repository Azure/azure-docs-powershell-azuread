---
title: Get-AzureADGroupOwner
description: This article provides migration details from Get-AzureADGroupOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADGroupOwner

This article provides migration details from Get-AzureADGroupOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADGroupOwner](/powershell/module/azuread/get-azureadgroupowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroupOwner](/powershell/module/microsoft.graph.groups/get-mggroupowner) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroupOwner))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  GET /groups/{group-id}/owners

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-list-owners-permissions.md)]

View more [details on permissions](/graph/api/group-list-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|