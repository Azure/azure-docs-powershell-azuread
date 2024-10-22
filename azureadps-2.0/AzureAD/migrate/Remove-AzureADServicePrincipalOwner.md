---
title: Remove-AzureADServicePrincipalOwner
description: This article provides migration details from Remove-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 12/16/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADServicePrincipalOwner

This article provides migration details from Remove-AzureADServicePrincipalOwner command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Remove-AzureADServicePrincipalOwner](/powershell/module/azuread/remove-azureadserviceprincipalowner)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Remove-MgServicePrincipalOwnerByRef](/powershell/module/microsoft.graph.applications/remove-mgserviceprincipalownerbyref) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Remove-MgServicePrincipalOwnerByRef))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  DELETE /servicePrincipals/{servicePrincipal-id}/owners/{directoryObject-id}/$ref

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-delete-owners-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-delete-owners#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ServicePrincipalId|
|OwnerId|DirectoryObjectId|