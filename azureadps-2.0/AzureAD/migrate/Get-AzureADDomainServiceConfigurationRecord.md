---
title: Get-AzureADDomainServiceConfigurationRecord
description: This article provides migration details from Get-AzureADDomainServiceConfigurationRecord command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDomainServiceConfigurationRecord

This article provides migration details from Get-AzureADDomainServiceConfigurationRecord command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDomainServiceConfigurationRecord](/powershell/module/azuread/get-azureaddomainserviceconfigurationrecord)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDomainServiceConfigurationRecord](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdomainserviceconfigurationrecord) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDomainServiceConfigurationRecord))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /domains/{domain-id}/serviceConfigurationRecords | /domains/{domain-id}/serviceConfigurationRecords/{domainDnsRecord-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-list-serviceconfigurationrecords-permissions.md)]

View more [details on permissions](/graph/api/domain-list-serviceconfigurationrecords#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|