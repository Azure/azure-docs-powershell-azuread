---
title: Remove-AzureADDomain
description: This article provides migration details from Remove-AzureADDomain command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADDomain

This article provides migration details from Remove-AzureADDomain command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADDomain](/powershell/module/azuread/remove-azureaddomain)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDomain](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdomain) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions q=Remove-MgDomain))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /domains/{domain-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-delete-permissions.md)]

View more [details on permissions](/graph/api/domain-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|