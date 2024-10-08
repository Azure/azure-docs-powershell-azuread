---
title: Add-AzureADServicePrincipalOwner
description: This article provides migration details from Add-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADServicePrincipalOwner

This article provides migration details from Add-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADServicePrincipalOwner](/powershell/module/azuread/add-azureadserviceprincipalowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgServicePrincipalOwnerByRef](/powershell/module/microsoft.graph.applications/new-mgserviceprincipalownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgServicePrincipalOwnerByRef))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  POST /servicePrincipals/{id}/owners/$ref

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Application.ReadWrite.All and Directory.Read.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Application.ReadWrite.OwnedBy and Directory.Read.All, Application.ReadWrite.All and Directory.Read.All |

View more [details on permissions](/graph/api/serviceprincipal-post-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ServicePrincipalId|
|RefObjectId|OdataId|