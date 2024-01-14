---
title: Get-AzureADDomainNameReference
description: This article provides migration details from Get-AzureADDomainNameReference command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDomainNameReference

This article provides migration details from Get-AzureADDomainNameReference command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDomainNameReference](/powershell/module/azuread/get-azureaddomainnamereference)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDomainNameReference](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdomainnamereference) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDomainNameReference))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: GET /domains/{id}/domainNameReferences

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-list-domainnamereferences-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|