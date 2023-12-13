---
title: Get-AzureADUserLicenseDetail
description: This article provides migration details from Get-AzureADUserLicenseDetail command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADUserLicenseDetail

This article provides migration details from Get-AzureADUserLicenseDetail command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADUserLicenseDetail](/powershell/module/azuread/get-azureaduserlicensedetail)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgUserLicenseDetail](/powershell/module/microsoft.graph.users/get-mguserlicensedetail) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgUserLicenseDetail))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  GET /users/{id}/licenseDetails

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-list-licensedetails-permissions.md)]

View more [details on permissions](/graph/api/user-list-licensedetails#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|UserId|