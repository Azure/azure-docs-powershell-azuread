---
title: Get-AzureADGroup
description: This article provides migration details from Get-AzureADGroup command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADGroup

This article provides migration details from Get-AzureADGroup command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADGroup](/powershell/module/azuread/get-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgGroup](/powershell/module/microsoft.graph.groups/get-mggroup) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgGroup))
+ Graph Module: Microsoft.Graph.Groups
+ Graph Endpoint:  GET /groups/{id}

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|GroupMember.Read.All|Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Group.Read.All|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|GroupMember.Read.All|Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Group.Read.All|

View more [details on permissions](/graph/api/group-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|Id|
|SearchString|NA|
|Top|Top|