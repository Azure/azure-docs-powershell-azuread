---
title: New-AzureADDomain
description: This article provides migration details from New-AzureADDomain command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADDomain

This article provides migration details from New-AzureADDomain command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADDomain](/powershell/module/azuread/new-azureaddomain)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDomain](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdomain) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDomain))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: POST /domains

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-post-domains-permissions.md)]

View more [details on permissions](/graph/api/domain-post-domains#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|IsDefault|IsDefault|
|IsDefaultForCloudRedirections||
|Name||
|SupportedServices|SupportedServices|