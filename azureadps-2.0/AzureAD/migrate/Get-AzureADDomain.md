---
title: Get-AzureADDomain
description: This article provides migration details from Get-AzureADDomain command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDomain

This article provides migration details from Get-AzureADDomain command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDomain](/powershell/module/azuread/get-azureaddomain)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDomain](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdomain) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDomain))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET  /domains | /domains/{domain-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-get-permissions.md)]

View more [details on permissions](/graph/api/domain-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|