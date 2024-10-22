---
title: Get-AzureADTenantDetail
description: This article provides migration details from Get-AzureADTenantDetail command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADTenantDetail

This article provides migration details from Get-AzureADTenantDetail command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADTenantDetail](/powershell/module/azuread/get-azureadtenantdetail)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgOrganization](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgorganization) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgOrganization))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  /organization | /organization/{organization-id}

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | User.Read, Organization.Read.All, Directory.Read.All, Organization.ReadWrite.All, Directory.ReadWrite.All   |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Organization.Read.All, Directory.Read.All, Organization.ReadWrite.All, Directory.ReadWrite.All |

View more [details on permissions](/graph/api/organization-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|NA|OrganizationId|
|Top|Top|