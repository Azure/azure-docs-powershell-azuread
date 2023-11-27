---
title: Set-AzureADUser
description: This article provides migration details from Set-AzureADUser command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 11/10/2023
ms.author: eunicewaweru
manager: CelesteDG
ms.reviewer: stevemutungi
---

# Set-AzureADUser

This article provides migration details from Set-AzureADUser command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADUser](https://docs.microsoft.com/en-us/powershell/module/AzureAD/Set-AzureADUser)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgUser](https://docs.microsoft.com/en-us/powershell/module/Microsoft.Graph.Users/Update-MgUser) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgUser))
+ Graph Module: Microsoft.Graph.Users
+ Graph Endpoint:  PATCH  /users/{user-id}

## Permissions

|Permission type|Least privileged permissions|Higher privileged permissions |
|---|---|---|
|Delegated (work or school account)|User.ReadWrite| User.ManageIdentities.All, User.EnableDisableAccount.All, User.ReadWrite.All, Directory.ReadWrite.All |
|Delegated (personal Microsoft account)|User.ReadWrite| Not available. |
|Application|User.ManageIdentities.All| User.EnableDisableAccount.All, User.ReadWrite.All, Directory.ReadWrite.All |

View more [details on permissions](/graph/api/user-update?view=graph-rest-1.0&tabs=http#permissions).

## Property Mapping

|AAD Name|Graph Name|
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