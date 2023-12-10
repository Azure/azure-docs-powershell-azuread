---
title: Add-AzureADDirectoryRoleMember
description: This article provides migration details from Add-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADDirectoryRoleMember

This article provides migration details from Add-AzureADDirectoryRoleMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADDirectoryRoleMember](/powershell/module/azuread/add-azureaddirectoryrolemember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDirectoryRoleMemberByRef](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdirectoryrolememberbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDirectoryRoleMemberByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: POST /directoryRoles/{directoryRole-id}/members/$ref

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|RoleManagement.ReadWrite.Directory|Not available.|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|RoleManagement.ReadWrite.Directory|Not available.|

View more [details on permissions](/graph/api/directoryrole-post-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DirectoryRoleId|
|RefObjectId|OdataId|