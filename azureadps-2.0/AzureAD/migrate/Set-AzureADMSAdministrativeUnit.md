---
title: Set-AzureADMSAdministrativeUnit
description: This article provides migration details from Set-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 11/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSAdministrativeUnit

This article provides migration details from Set-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSAdministrativeUnit](/powershell/module/azuread/set-azureadmsadministrativeunit)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgDirectoryAdministrativeUnit](/powershell/module/microsoft.graph.identity.directorymanagement/update-mgdirectoryadministrativeunit) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgDirectoryAdministrativeUnit))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  PATCH /directory/administrativeUnits/{administrativeUnit-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/administrativeunit-update-permissions.md)]

View more [details on permissions](/graph/api/administrativeunit-update#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|AdministrativeUnitId|