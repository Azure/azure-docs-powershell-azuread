---
title: Get-AzureADContactDirectReport
description: This article provides migration details from Get-AzureADContactDirectReport command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADContactDirectReport

This article provides migration details from Get-AzureADContactDirectReport command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADContactDirectReport](/powershell/module/azuread/get-azureadcontactdirectreport)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgContactDirectReport](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgcontactdirectreport) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgContactDirectReport))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: GET /contacts/{orgContact-id}/directReports | /contacts/{orgContact-id}/directReports/{directoryObject-id}

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | OrgContact.Read.All and Group.Read.All, Directory.Read.All  |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | OrgContact.Read.All and Group.Read.All, Directory.Read.All |

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|OrgContactId|
|All|All|
|Top|Top|