---
title: Confirm-AzureADDomain
description: This article provides migration details from Confirm-AzureADDomain command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Confirm-AzureADDomain

This article provides migration details from Confirm-AzureADDomain command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Confirm-AzureADDomain](/powershell/module/azuread/confirm-azureaddomain)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Confirm-MgDomain](/powershell/module/microsoft.graph.identity.directorymanagement/confirm-mgdomain) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Confirm-MgDomain))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  POST /domains/{domain-id}/verify

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-verify-permissions.md)]

View more [details on permissions](/graph/api/domain-verify#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|