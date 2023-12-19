---
title: Get-AzureADContact
description: This article provides migration details from Get-AzureADContact command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADContact

This article provides migration details from Get-AzureADContact command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADContact](/powershell/module/azuread/get-azureadcontact)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgContact](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgcontact) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgContact))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /contacts/{orgContact-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/orgcontact-get-permissions.md)]

View more [details on permissions](/graph/api/orgcontact-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|ObjectId|OrgContactId|
|Top|Top|