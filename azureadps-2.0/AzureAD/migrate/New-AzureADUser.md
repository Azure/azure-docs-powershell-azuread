---
title: New-AzureADUser
description: This article provides migration details from New-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 12/13/2023
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# New-AzureADUser

This article provides migration details from New-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [New-AzureADUser](/powershell/module/azuread/new-azureaduser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [New-MgUser](/powershell/module/microsoft.graph.users/new-mguser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=New-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint: POST /users

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-post-users-permissions.md)]

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