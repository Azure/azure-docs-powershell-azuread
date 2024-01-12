---
title: Get-AzureADApplicationServiceEndpoint
description: This article provides migration details from Get-AzureADApplicationServiceEndpoint command to Microsoft Graph PowerShell.

ms.service: active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADApplicationServiceEndpoint

This article provides migration details from Get-AzureADApplicationServiceEndpoint command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADApplicationServiceEndpoint](/powershell/module/azuread/get-azureadapplicationserviceendpoint)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgServicePrincipalEndpoint](/powershell/module/microsoft.graph.applications/get-mgserviceprincipalendpoint) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgServicePrincipalEndpoint))
+ Graph Module: Microsoft.Graph.Applications
+ Graph Endpoint: GET /servicePrincipals/{servicePrincipal-id}/endpoints | /servicePrincipals/{servicePrincipal-id}/endpoints/{endpoint-id}

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|ServicePrincipalId|
|All|All|
|Top|Top|