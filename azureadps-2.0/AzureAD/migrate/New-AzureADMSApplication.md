---
title: New-AzureADMSApplication
description: This article provides migration details from New-AzureADMSApplication command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/18/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADMSApplication

This article provides migration details from New-AzureADMSApplication command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADMSApplication](/powershell/module/azuread/new-azureadmsapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgApplication](/powershell/module/microsoft.graph.applications/new-mgapplication) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgApplication))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: POST /applications

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-post-applications-permissions.md)]

View more [details on permissions](/graph/api/application-post-applications#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AddIns|AddIns|
|AllowGuestsSignIn||
|AllowPassthroughUsers||
|AppLogoUrl||
|AppRoles|AppRoles|
|AvailableToOtherTenants||
|DisplayName|DisplayName|
|ErrorUrl||
|GroupMembershipClaims|GroupMembershipClaims|
|Homepage||
|IdentifierUris|IdentifierUris|
|InformationalUrls||
|IsDeviceOnlyAuthSupported|IsDeviceOnlyAuthSupported|
|IsDisabled||
|KeyCredentials|KeyCredentials|
|KnownClientApplications||
|LogoutUrl||
|Oauth2AllowImplicitFlow||
|Oauth2AllowUrlPathMatching||
|Oauth2Permissions||
|Oauth2RequirePostResponse|Oauth2RequirePostResponse|
|OptionalClaims|OptionalClaims|
|OrgRestrictions||
|ParentalControlSettings|ParentalControlSettings|
|PasswordCredentials|PasswordCredentials|
|PreAuthorizedApplications||
|PublicClient|PublicClient|
|PublisherDomain|PublisherDomain|
|RecordConsentConditions||
|ReplyUrls||
|RequiredResourceAccess|RequiredResourceAccess|
|SamlMetadataUrl|SamlMetadataUrl|
|SignInAudience|SignInAudience|
|WwwHomepage||