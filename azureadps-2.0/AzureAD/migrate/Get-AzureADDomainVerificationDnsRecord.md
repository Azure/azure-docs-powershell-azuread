---
title: Get-AzureADDomainVerificationDnsRecord
description: This article provides migration details from Get-AzureADDomainVerificationDnsRecord command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDomainVerificationDnsRecord

This article provides migration details from Get-AzureADDomainVerificationDnsRecord command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDomainVerificationDnsRecord](/powershell/module/azuread/get-azureaddomainverificationdnsrecord)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDomainVerificationDnsRecord](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdomainverificationdnsrecord) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDomainVerificationDnsRecord))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: GET /domains/{id}/verificationDnsRecords

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/domain-list-verificationdnsrecords-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Name|DomainId|