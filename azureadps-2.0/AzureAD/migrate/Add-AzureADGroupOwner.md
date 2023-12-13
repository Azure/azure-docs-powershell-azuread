---
title: Add-AzureADGroupOwner
description: This article provides migration details from Add-AzureADGroupOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADGroupOwner

This article provides migration details from Add-AzureADGroupOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADGroupOwner](/powershell/module/azuread/add-azureadgroupowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgGroupOwnerByRef](/powershell/module/microsoft.graph.groups/new-mggroupownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgGroupOwnerByRef))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint: POST /groups/{group-id}/owners/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-post-owners-permissions.md)]

View more [details on permissions](/graph/api/group-post-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|RefObjectId|OdataId|