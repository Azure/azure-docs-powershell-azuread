---
title: New-AzureADMSAdministrativeUnit
description: This article provides migration details from New-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSAdministrativeUnit

This article provides migration details from New-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSAdministrativeUnit](/powershell/module/azuread/new-azureadmsadministrativeunit)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDirectoryAdministrativeUnit](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdirectoryadministrativeunit) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDirectoryAdministrativeUnit))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint: POST /directory/administrativeUnits

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/directory-post-administrativeunits-permissions.md)]

View more [details on permissions](/graph/api/directory-post-administrativeunits#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Description|Description|
|DisplayName|DisplayName|