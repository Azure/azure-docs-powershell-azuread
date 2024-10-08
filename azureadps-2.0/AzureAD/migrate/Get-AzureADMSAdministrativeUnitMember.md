---
title: Get-AzureADMSAdministrativeUnitMember
description: This article provides migration details from Get-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSAdministrativeUnitMember

This article provides migration details from Get-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADMSAdministrativeUnitMember](/powershell/module/azuread/get-azureadmsadministrativeunitmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDirectoryAdministrativeUnitMember](/powershell/module/microsoft.graph.identity.directorymanagement/get-mgdirectoryadministrativeunitmember) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDirectoryAdministrativeUnitMember))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  GET /directory/administrativeUnits/{administrativeUnit-id}/members

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/administrativeunit-get-members-permissions.md)]

View more [details on permissions](/graph/api/administrativeunit-get-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|All|All|
|Id|AdministrativeUnitId|
|Top|Top|