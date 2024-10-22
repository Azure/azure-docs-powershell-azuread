---
title: Remove-AzureADMSAdministrativeUnit
description: This article provides migration details from Remove-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSAdministrativeUnit

This article provides migration details from Remove-AzureADMSAdministrativeUnit command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSAdministrativeUnit](/powershell/module/azuread/remove-azureadmsadministrativeunit)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDirectoryAdministrativeUnit](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdirectoryadministrativeunit) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgDirectoryAdministrativeUnit))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  DELETE /directory/administrativeUnits/{administrativeUnit-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/administrativeunit-delete-permissions.md)]

View more [details on permissions](/graph/api/administrativeunit-delete#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|AdministrativeUnitId|