---
title: Get-AzureADMSApplicationOwner
description: This article provides migration details from Get-AzureADMSApplicationOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSApplicationOwner

This article provides migration details from Get-AzureADMSApplicationOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSApplicationOwner](/powershell/module/azuread/get-azureadmsapplicationowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgApplicationOwner](/powershell/module/microsoft.graph.applications/get-mgapplicationowner) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgApplicationOwner))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  GET /applications/{id}/owners

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|Application.Read.All|Application.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|Application.ReadWrite.OwnedBy|Application.Read.All, Application.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All|

View more [details on permissions](/graph/api/application-list-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|ObjectId|ApplicationId|
|Top|Top|