---
title: Remove-AzureADMSAdministrativeUnitMember
description: This article provides migration details from Remove-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSAdministrativeUnitMember

This article provides migration details from Remove-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADMSAdministrativeUnitMember](/powershell/module/azuread/remove-azureadmsadministrativeunitmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgDirectoryAdministrativeUnitMemberByRef](/powershell/module/microsoft.graph.identity.directorymanagement/remove-mgdirectoryadministrativeunitmemberbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgDirectoryAdministrativeUnitMemberByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  PATCH /directory/administrativeUnits/{administrativeUnit-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/administrativeunit-delete-members-permissions.md)]

View more [details on permissions](/graph/api/administrativeunit-delete-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|AdministrativeUnitId|
|MemberId|DirectoryObjectId|