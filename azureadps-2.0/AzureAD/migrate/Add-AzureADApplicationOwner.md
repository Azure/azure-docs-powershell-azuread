---
title: Add-AzureADApplicationOwner
description: This article provides migration details from Add-AzureADApplicationOwner command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADApplicationOwner

This article provides migration details from Add-AzureADApplicationOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADApplicationOwner](/powershell/module/azuread/add-azureadapplicationowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgApplicationOwnerByRef](/powershell/module/microsoft.graph.applications/new-mgapplicationownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgApplicationOwnerByRef))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  POST /applications/{application-id}/owners/$ref

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Application.ReadWrite.All and Directory.Read.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Application.ReadWrite.OwnedBy and Directory.Read.All, Application.ReadWrite.All and Directory.Read.All |

> **Note:** **Application.ReadWrite.OwnedBy** will not be sufficient to add another owner. Consent also to **Application.ReadWrite.All**. 

View more [details on permissions](/graph/api/application-post-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|
|RefObjectId|OdataId|