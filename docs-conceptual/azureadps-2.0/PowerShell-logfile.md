---
services: active-directory
documentationcenter: ''
title: 'Log file'
ms.service: azure-active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
ms.reviewer: stevemutungi
description: Discover how to locate and utilize the PowerShell log file for Azure AD diagnostics. Learn to analyze errors and track cmdlet execution paths.
---
# Where can I find the PowerShell log file?

Azure AD PowerShell maintains a log file for diagnostic purposes. You can find this file here:

```powershell
C:\Users\<alias>\AppData\Local\Microsoft\AzureAD\Powershell\AzureADPowershell_<sessionStartTimeStamp>.log
```

The log file contains a time stamped record of all actions a cmdlet has executed. You can use this to analyze errors or just follow the execution path of a cmdlet or script.
