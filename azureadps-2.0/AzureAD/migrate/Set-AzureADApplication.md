---
title: Set-AzureADApplication
description: This article provides migration details from Set-AzureADApplication command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/19/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADApplication

This article provides migration details from Set-AzureADApplication command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADApplication](/powershell/module/azuread/set-azureadapplication)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgApplication](/powershell/module/microsoft.graph.applications/update-mgapplication) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgApplication))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint:  PATCH /applications/{application-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/application-update-permissions.md)]

View more [details on permissions](/graph/api/application-update#permissions).

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