---
title: Get-AzureADDeviceConfiguration
description: This article provides migration details from Get-AzureADDeviceConfiguration command to Microsoft Graph PowerShell.

ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/12/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADDeviceConfiguration

This article provides migration details from Get-AzureADDeviceConfiguration command to Microsoft Graph PowerShell.

## Summary

+ Azure AD Command: [Get-AzureADDeviceConfiguration](/powershell/module/azuread/get-azureaddeviceconfiguration)
+ Azure AD Module: AzureAD
+ Microsoft Graph Command: [Get-MgDeviceManagementDeviceConfiguration](/powershell/module/microsoft.graph.devicemanagement/get-mgdevicemanagementdeviceconfiguration) ([Community Examples](https://github.com/orgs/msgraph/discussions?discussions_q=Get-MgDeviceManagementDeviceConfiguration))
+ Graph Module: Microsoft.Graph.DeviceManagement
+ Graph Endpoint: GET /deviceManagement/deviceConfigurations | /deviceManagement/deviceConfigurations/{deviceConfiguration-id}

## Permissions

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All|

## Property Mapping

|Azure AD Name|Microsoft Graph Name|
|---|---|
|ObjectId|DeviceConfigurationId|