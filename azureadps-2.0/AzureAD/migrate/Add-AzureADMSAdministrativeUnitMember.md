---
title: Add-AzureADMSAdministrativeUnitMember
description: This article provides migration details from Add-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/13/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADMSAdministrativeUnitMember

This article provides migration details from Add-AzureADMSAdministrativeUnitMember command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADMSAdministrativeUnitMember](/powershell/module/azuread/add-azureadmsadministrativeunitmember)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgDirectoryAdministrativeUnitMemberByRef](/powershell/module/microsoft.graph.identity.directorymanagement/new-mgdirectoryadministrativeunitmemberbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgDirectoryAdministrativeUnitMemberByRef))
+ Graph Module: Microsoft.Graph.Identity.DirectoryManagement
+ Graph Endpoint:  POST /directory/administrativeUnits/{administrativeUnit-id}/members/$ref

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | AdministrativeUnit.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | AdministrativeUnit.ReadWrite.All |

To add a user, group, or device to an administrative unit, the calling principal must be assigned one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

* Privileged Role Administrator

### Permissions to create a new group

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Group.Create, Group.ReadWrite.All, Directory.ReadWrite.All |

To create a new group in an administrative unit, the calling principal must be assigned one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

* Privileged Role Administrator
* Groups Administrator

View more [details on permissions](/graph/api/administrativeunit-post-members#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|Id|AdministrativeUnitId|
|RefObjectId|OdataId|