---
services: active-directory
documentationcenter: ''
title: 'How to recover deleted data'
ms.service: azure-active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
ms.reviewer: stevemutungi
---
# Recovering deleted data
If you have accidentally deleted data from your directory there may be some options for recovering the lost data using PowerShell. You can recover deleted Applications and deleted Unified Groups in the first 30 days after deletion. This article describes how to do that.

## Finding deleted Unified groups
To find the deleted Unified groups in your directory you can use the Get-AzureADMSDeletedGroup cmdlets. This cmdlet returns all Unified Group objects that were deleted in the past 30 days. Here is an example of the cmdlet and its output:

```powershell
Get-AzureADMSDeletedGroup

Id                                   DisplayName         Description
--                                   -----------         -----------
1dc315b7-9ed4-468f-a190-1d90442e43f8 SpeedTest9
1e26b664-3f47-4e21-8045-78ee7d67e69f SpeedTest1992
```

To find all deleted Application objects, you can use Get-AzureADMSApplication:

```powershell
PS C:\WINDOWS\system32> Get-AzureADDeletedApplication

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 00001111-aaaa-2222-bbbb-3333cccc4444 My Properties Bag
```

Within the first 30 days after an object is deleted, it can be recovered using the Recover-AzureADMSDeletedDirectoryObject cmdlet. To recover a deleted directory pobject you must specify the Id of the object. This is what you see when you recover a deleted group:

```powershell
Restore-AzureADMSDeletedDirectoryObject -Id 822cda93-4d5b-4c60-86d9-5d395e37afb4

Id                                   DisplayName     Description
--                                   -----------     -----------
822cda93-4d5b-4c60-86d9-5d395e37afb4 XSpeedTest1996A XSpeedTest1996A
```
To recover all deleted Unified Groups you would use
```powershell
Get-AzureADMSDeletedGroup | Restore-AzureADMSDeletedDirectoryObject
```
The first cmdlet will retrieve the deleted unified groups in your directory, the second cmdlet will be executed for each deleted group and will restore the deleted groups.

If you want to recover a deleted application object, you can use

```powershell
Restore-AzureADDeletedApplication -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 00001111-aaaa-2222-bbbb-3333cccc4444 My Properties Bag
```

If you want to permanently delete a unified group to prevent anyone from recovering it, you can use
```powershell
Remove-AzureADMSDeletedDirectoryObject -Id 854e0412-6975-4ac0-94a3-9bfff671b7f8
```

>Note: If you attempt to recover a deleted unified group for which the SAMAccountName already exists the cmdlet will fail. You must first remove the existing SAMAccountName by either changing it or deleting the object that has it.
>
