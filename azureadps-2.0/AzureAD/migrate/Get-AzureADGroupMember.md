---
title: Get-AzureADGroupMember
description: This article provides migration details from Get-AzureADGroupMember command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADGroupMember

This article provides migration details from Get-AzureADGroupMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADGroupMember](/powershell/module/azuread/get-azureadgroupmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroupMember](/powershell/module/microsoft.graph.groups/get-mggroupmember) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroupMember))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  GET /groups/{id}/members

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-list-members-permissions.md)]

View more [details on permissions](/graph/api/group-list-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|