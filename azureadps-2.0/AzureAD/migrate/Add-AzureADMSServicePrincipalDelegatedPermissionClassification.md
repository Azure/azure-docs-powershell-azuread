---
title: Add-AzureADMSServicePrincipalDelegatedPermissionClassification
description: This article provides migration details from Add-AzureADMSServicePrincipalDelegatedPermissionClassification command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/28/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Add-AzureADMSServicePrincipalDelegatedPermissionClassification

This article provides migration details from Add-AzureADMSServicePrincipalDelegatedPermissionClassification command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Add-AzureADMSServicePrincipalDelegatedPermissionClassification](/powershell/module/azuread/add-azureadmsserviceprincipaldelegatedpermissionclassification)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgServicePrincipalDelegatedPermissionClassification](/powershell/module/microsoft.graph.applications/new-mgserviceprincipaldelegatedpermissionclassification) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgServicePrincipalDelegatedPermissionClassification))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /servicePrincipals/{servicePrincipal-id}/delegatedPermissionClassifications

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-post-delegatedpermissionclassifications-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-post-delegatedpermissionclassifications#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ServicePrincipalId|ServicePrincipalId|
|Classification|Classification|
|PermissionId|PermissionId|
|PermissionName|PermissionName|