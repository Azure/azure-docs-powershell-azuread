---
title: New-AzureADServicePrincipal
description: This article provides migration details from New-AzureADServicePrincipal command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADServicePrincipal

This article provides migration details from New-AzureADServicePrincipal command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADServicePrincipal](/powershell/module/azuread/new-azureadserviceprincipal)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgServicePrincipal](/powershell/module/microsoft.graph.applications/new-mgserviceprincipal) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgServicePrincipal))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /servicePrincipals

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/serviceprincipal-post-serviceprincipals-permissions.md)]

View more [details on permissions](/graph/api/serviceprincipal-post-serviceprincipals#permissions).

For multi-tenant apps, the calling user must also be in one of the following [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference?toc=%2Fgraph%2Ftoc.json):

+ Application Administrator
+ Cloud Application Administrator roles

For single-tenant apps where the calling user is a non-admin user but is the owner of the backing application, the user must have the *Application Developer* role.


## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AccountEnabled|AccountEnabled|
|AlternativeNames|AlternativeNames|
|AppId|AppId|
|AppRoleAssignmentRequired|AppRoleAssignmentRequired|
|ErrorUrl|NA|
|Homepage|Homepage|
|KeyCredentials|KeyCredentials|
|LogoutUrl|LogoutUrl|
|PasswordCredentials|PasswordCredentials|
|PublisherName|NA|
|ReplyUrls|ReplyUrls|
|DisplayName|DisplayName|
|SamlMetadataUrl|NA|
|ServicePrincipalNames|ServicePrincipalNames|
|ServicePrincipalType|ServicePrincipalType|
|Tags|Tags|