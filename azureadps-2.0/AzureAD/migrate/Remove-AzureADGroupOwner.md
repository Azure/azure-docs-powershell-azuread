---
title: Remove-AzureADGroupOwner
description: This article provides migration details from Remove-AzureADGroupOwner command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADGroupOwner

This article provides migration details from Remove-AzureADGroupOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADGroupOwner](/powershell/module/azuread/remove-azureadgroupowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgGroupOwnerByRef](/powershell/module/microsoft.graph.groups/remove-mggroupownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgGroupOwnerByRef))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  DELETE /groups/{group-id}/owners/{directoryObject-id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-delete-owners-permissions.md)]

View more [details on permissions](/graph/api/group-delete-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|OwnerId|DirectoryObjectId|