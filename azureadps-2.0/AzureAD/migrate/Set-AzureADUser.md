---
title: Set-AzureADUser
description: This article provides migration details from Set-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADUser

This article provides migration details from Set-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADUser](/powershell/module/azuread/set-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgUser](/powershell/module/microsoft.graph.users/update-mguser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  PATCH  /users/{user-id}

## Permissions

View more [details on permissions](/graph/api/user-update#permissions).

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AccountEnabled|AccountEnabled|
|AgeGroup|AgeGroup|
|City|City|
|CompanyName|CompanyName|
|ConsentProvidedForMinor|ConsentProvidedForMinor|
|Country|Country|
|CreationType|CreationType|
|Department|Department|
|DisplayName|DisplayName|
|ExtensionProperty||
|FacsimileTelephoneNumber||
|GivenName|GivenName|
|ImmutableId||
|IsCompromised||
|JobTitle|JobTitle|
|MailNickName|MailNickname|
|Mobile||
|ObjectId||
|OtherMails|OtherMails|
|PasswordPolicies|PasswordPolicies|
|PasswordProfile|PasswordProfile|
|PhysicalDeliveryOfficeName||
|PostalCode|PostalCode|
|PreferredLanguage|PreferredLanguage|
|ShowInAddressList|ShowInAddressList|
|SignInNames||
|State|State|
|StreetAddress|StreetAddress|
|Surname|Surname|
|TelephoneNumber||
|UsageLocation|UsageLocation|
|UserPrincipalName|UserPrincipalName|
|UserState||
|UserStateChangedOn||
|UserType|UserType|
