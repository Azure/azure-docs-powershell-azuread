---
title: Add-AzureADGroupMember
description: This article provides migration details from Add-AzureADGroupMember command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADGroupMember

This article provides migration details from Add-AzureADGroupMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADGroupMember](/powershell/module/azuread/add-azureadgroupmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgGroupMember](/powershell/module/microsoft.graph.groups/new-mggroupmember) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgGroupMember))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint: POST /groups/{group-id}/members/$ref

## Permissions

|Delegated|Delegated (personal Microsoft account)|Application|
|:---|:---|:---|
|GroupMember.ReadWrite.All and Device.ReadWrite.All|Not supported.|GroupMember.ReadWrite.All and Device.ReadWrite.All.|

View more [details on permissions](/graph/api/group-post-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|GroupId|
|RefObjectId|DirectoryObjectId|