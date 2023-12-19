---
title: Remove-AzureADDirectoryRoleMember
description: This article provides migration details from Remove-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADDirectoryRoleMember

This article provides migration details from Remove-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADDirectoryRoleMember](/powershell/module/azuread/remove-azureaddirectoryrolemember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDirectoryRoleMemberByRef](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdirectoryrolememberbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgDirectoryRoleMemberByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /directoryRoles/{role-id}/members/{id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directoryrole-delete-member-permissions.md)]

View more [details on permissions](/graph/api/directoryrole-delete-member#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DirectoryRoleId|
|UserId|DirectoryObjectId|