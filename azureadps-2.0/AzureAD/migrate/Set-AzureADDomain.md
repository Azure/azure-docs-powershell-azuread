---
title: Set-AzureADDomain
description: This article provides migration details from Set-AzureADDomain command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADDomain

This article provides migration details from Set-AzureADDomain command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADDomain](/powershell/module/azuread/set-azureaddomain)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgDomain](/powershell/module/microsoft.graph.identity.directorymanagement/update-mgdomain) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgDomain))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  PATCH /domains/{domain-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-update-permissions.md)]

View more [details on permissions](/graph/api/domain-update#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|IsDefault|IsDefault|
|IsDefaultForCloudRedirections||
|Name||
|SupportedServices|SupportedServices|