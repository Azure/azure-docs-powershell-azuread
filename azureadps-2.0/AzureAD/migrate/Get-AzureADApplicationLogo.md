---
title: Get-AzureADApplicationLogo
description: This article provides migration details from Get-AzureADApplicationLogo command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADApplicationLogo

This article provides migration details from Get-AzureADApplicationLogo command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADApplicationLogo](/powershell/module/azuread/get-azureadapplicationlogo)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgApplicationLogo](/powershell/module/microsoft.graph.applications/get-mgapplicationlogo) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgApplicationLogo))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: GET /applications/{application-id}/logo

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ApplicationId|
|FileName|NA|
|FilePath|NA|
|View|NA|