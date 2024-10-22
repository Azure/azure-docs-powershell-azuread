---
title: Set-AzureADMSAuthorizationPolicy
description: This article provides migration details from Set-AzureADMSAuthorizationPolicy command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Set-AzureADMSAuthorizationPolicy

This article provides migration details from Set-AzureADMSAuthorizationPolicy command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Set-AzureADMSAuthorizationPolicy](/powershell/module/azuread/set-azureadmsauthorizationpolicy)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Update-MgPolicyAuthorizationPolicy](/powershell/module/microsoft.graph.identity.signins/update-mgpolicyauthorizationpolicy) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Update-MgPolicyAuthorizationPolicy))
+ Graph Module: Microsoft.Graph.Identity.SignIns
+ Graph Endpoint:  PATCH /policies/authorizationPolicy | /policies/authorizationPolicy/{authorizationPolicy-id}

## Permissions

[!INCLUDE [permissions-table](~/graphref/api-reference/v1.0/includes/permissions/authorizationpolicy-update-permissions.md)]

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|AllowedToSignUpEmailBasedSubscriptions|AllowedToSignUpEmailBasedSubscriptions|
|AllowedToUseSSPR|AllowedToUseSSPR|
|AllowEmailVerifiedUsersToJoinOrganization|AllowEmailVerifiedUsersToJoinOrganization|
|BlockMsolPowerShell|BlockMsolPowerShell|
|DefaultUserRolePermissions|DefaultUserRolePermissions|
|DefaultUserRolePermissions|DefaultUserRolePermissions|
|DisplayName|DisplayName|
|Description|Description|