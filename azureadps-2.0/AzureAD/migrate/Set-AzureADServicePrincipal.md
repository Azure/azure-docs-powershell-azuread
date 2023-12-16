---
title: Set-AzureADServicePrincipal
description: This article provides migration details from Set-AzureADServicePrincipal command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADServicePrincipal

This article provides migration details from Set-AzureADServicePrincipal command to Microsoft Graph PowerShell.

> [!IMPORTANT]
> Using PATCH to set [**passwordCredential**](/graph/api/resources/passwordcredential) is not supported. Use the [addPassword](/graph/api/serviceprincipal-addpassword) and [removePassword](/graph/api/serviceprincipal-removepassword) methods to update the password or secret for a servicePrincipal.

## Summary

+ Azure AD Command: [Set-AzureADServicePrincipal](/powershell/module/azuread/set-azureadserviceprincipal)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgServicePrincipal](/powershell/module/microsoft.graph.applications/update-mgserviceprincipal) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgServicePrincipal))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  PATCH /servicePrincipals/{servicePrincipal-id}

## Permissions

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Application.ReadWrite.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Application.ReadWrite.OwnedBy, Application.ReadWrite.All |

View more [details on permissions](/graph/api/serviceprincipal-update#permissions).

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