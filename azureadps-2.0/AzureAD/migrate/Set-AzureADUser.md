---
title: Set-AzureADUser
description: This article provides migration details from Set-AzureADUser command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
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

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/user-update-permissions.md)]

View more [details on permissions](/graph/api/user-update#permissions).

>[!NOTE]
> - To update sensitive user properties, such as **accountEnabled**, **mobilePhone**, and **otherMails** for users with privileged administrator roles:
>   - In delegated scenarios, the app must be assigned the *Directory.AccessAsUser.All* delegated permission and the calling user must have a higher privileged administrator role as indicated in [Who can perform sensitive actions](/graph/api/resources/users#who-can-perform-sensitive-actions).
>   - In app-only scenarios, the app must be assigned a higher privileged administrator role as indicated in [Who can perform sensitive actions](/graph/api/resources/users#who-can-perform-sensitive-actions).
> - Your personal Microsoft account must be tied to a Microsoft Entra tenant to update your profile with the *User.ReadWrite* delegated permission on a personal Microsoft account.
> - Updating the **identities** property requires the *User.ManageIdentities.All* permission. Also, adding a [B2C local account](/graph/api/resources/objectidentity) to an existing **user** object is not allowed, unless the **user** object already contains a local account identity.

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
