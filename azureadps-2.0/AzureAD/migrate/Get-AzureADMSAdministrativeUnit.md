---
title: Get-AzureADMSAdministrativeUnit
description: This article provides migration details from Get-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSAdministrativeUnit

This article provides migration details from Get-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSAdministrativeUnit](/powershell/module/azuread/get-azureadmsadministrativeunit)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryAdministrativeUnit](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectoryadministrativeunit) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryAdministrativeUnit))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /directory/administrativeUnits | /directory/administrativeUnits/{administrativeUnit-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/administrativeunit-get-permissions.md)]

View more [details on permissions](/graph/api/administrativeunit-get#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Filter|Filter|
|Id|AdministrativeUnitId|
|Top|Top|