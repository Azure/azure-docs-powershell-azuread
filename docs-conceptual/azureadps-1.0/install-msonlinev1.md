---
services: active-directory
title: 'Install MSOnline'
description: Provides a guide on the installation steps for MSOnline PowerShell.
ms.service: active-directory
ms.workload: identity
ms.devlang: powershell
ms.topic: article
ms.date: 01/21/2022
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
---
# Azure Active Directory (MSOnline)

>[!IMPORTANT]
> MSOnline is planned for deprecation on **March 30, 2024**. For more details on the deprecation plans, see the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-azure-ad-blog/microsoft-entra-new-feature-and-change-announcements/ba-p/3796396). We encourage you to continue migrating to [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview), which is the recommended module for interacting with Azure AD. In addition, Microsoft Graph PowerShell allows you access to all Microsoft Graph APIs and is available on PowerShell 7. For answers to frequent migration queries, see the [Migration FAQ](../azureadps-2.0/migration-faq.yml).

You can use MSOnline for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.

## Install MSOnline

MSonline is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

The easiest way to install the module is from the [PowerShell Gallery](https://www.powershellgallery.com/packages/MSOnline). You can install the module with the Install-Module cmdlet:

```powershell
Install-Module MSOnline
```

## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-MsolService** at the Windows PowerShell command prompt.
You will then be prompted for your credentials.
If you want, you can supply your credentials in advance, for example:

```PowerShell
$Msolcred = Get-credential
Connect-MsolService -Credential $MsolCred
```

The first command prompts for credentials and stores them as *$Msolcred*.
The next command uses those credentials as *$Msolcred* to connect to the service.

To connect to a specific environment of Azure Active Directory, use the **AzureEnvironment** parameter, as follows:

```powershell
Connect-MsolService -AzureEnvironment "AzureGermanyCloud"
```

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

## See also

- [Install the Microsoft Graph PowerShell SDK](/powershell/microsoftgraph/installation?view=graph-powershell-1.0&preserve-view=true)