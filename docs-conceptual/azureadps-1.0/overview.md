---
services: active-directory
documentationcenter: ''
title: 'MSOnline PowerShell overview'
description: Provides a description and getting started information for MSOline PowerShell.
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: billmath
ms.custom: posh-docs-conceptual
---

# Azure Active Directory (MSOnline)

>[!IMPORTANT]
> Azure AD and MSOnline PowerShell modules are deprecated as of March 30, 2024. To learn more, read the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-blog/important-azure-ad-graph-retirement-and-powershell-module/ba-p/3848270). After this date, support for these modules are limited to migration assistance to Microsoft Graph PowerShell SDK and security fixes. The deprecated modules will continue to function through March, 30 2025.
>
> We recommend migrating to [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview) to interact with Microsoft Entra ID (formerly Azure AD). For common migration questions, refer to the [Migration FAQ](/powershell/azure/active-directory/migration-faq). *Note:* Versions 1.0.x of MSOnline may experience disruption after June 30, 2024.

You can use MSOnline cmdlets for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.

## Install MSOnline

The MSOnline module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

You can install this module from the [PowerShell Gallery](https://www.powershellgallery.com/packages/MSOnline).

## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-MsolService** at the Windows PowerShell command prompt.
You will then be prompted for your credentials.
If you want, you can supply your credentials in advance, for example:

```PowerShell
$Msolcred = Get-credential
Connect-MsolService -Credential $MsolCred
```

The first command prompts for credentials and stores them as $Msolcred.
The next command uses those credentials as $Msolcred to connect to the service.

To connect to a specific environment of Azure Active Directory, use the AzureEnvironment parameter, as follows:

`Connect-MsolService -AzureEnvironment "AzureGermanyCloud"`

This example connects your PowerShell session to the German AzureAD environment.

See [Connect-MsolService](/powershell/module/msonline/connect-msolservice) for more information.

For more information about the cmdlets, you can do the following:

* To create a folder for help, list the cmdlets, and then open the file in notepad, you can run the following commands at the Windows PowerShell command prompt:

```PowerShell
New-Item c:\MsolHelp -Type directory
Get-command | Where-Object {$_.name -like "*msol*"} | Format-List | Out-File c:\MsolHelp\msolcmdlets.txt
Notepad c:\MsolHelp\msolcmdlets.txt
```

* View the examples for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Examples`

* View the name, synopsis, description, parameter descriptions, and any examples provided for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Detailed`

* View the name, synopsis, description, detailed parameters, and any examples provided for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Full`

>[!NOTE]
>MSOnline PowerShell can only be used by users who are a member of the directory. Guest users cannot use MSOnline PowerShell.

## More about Windows PowerShell

Windows PowerShell is a task-based command-line shell and scripting language designed for system administration.
Unlike most shells, which accept and return text, Windows PowerShell is built on top of the .NET Framework, and accepts and returns .NET Framework objects.

Windows PowerShell introduces the concept of a cmdlet (pronounced "command-let"), a simple, single-function command-line tool built into the shell.

Cmdlets have the following naming convention: a verb and noun separated by a dash (-), such as Get-Help, Get-Process, and Start-Service.

Windows PowerShell includes more than one hundred basic core cmdlets.
For more information about Windows PowerShell, see [Getting Started with Windows PowerShell](https://msdn.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell).

