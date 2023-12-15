---
title: Remove-AzureADGroupMember
description: This article provides migration details from Remove-AzureADGroupMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADGroupMember

This article provides migration details from Remove-AzureADGroupMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADGroupMember](/powershell/module/azuread/remove-azureadgroupmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgGroupMemberByRef](/powershell/module/microsoft.graph.groups/remove-mggroupmemberbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions q=Remove-MgGroupMemberByRef))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  DELETE /groups/{group-id}/members/{directoryObject-id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/group-delete-members-permissions.md)]

View more [details on permissions](/graph/api/group-delete-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|MemberId|DirectoryObjectId|