---
services: active-directory
documentationcenter: ''
title: 'Overview MSOnline'
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: billmath
ms.custom: posh-docs-conceptual

---


# Azure ActiveDirectory (MSOnline)

You can use the Azure Active Directory Module for Windows PowerShell cmdlets for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.

Please note that we will begin to deprecate this module when the functionality of this module is migrated to the newer [Azure Active Directory PowerShell for Graph Module](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0). We advise customers who are creating new PowerShell scripts to use the newer module instead of this module.

## Install the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

You can install this module from the [PowerShell Gallery](https://www.powershellgallery.com/packages/MSOnline)

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

See [Connect-MsolService](https://msdn.microsoft.com/library/azure/dn194123(v=azure.98).aspx) for more information.

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
