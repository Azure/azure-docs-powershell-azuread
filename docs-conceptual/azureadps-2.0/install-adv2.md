---
services: active-directory
documentationcenter: ''
title: 'Install AzureAD PowerShell for Graph'
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
---
# Install Azure Active Directory PowerShell for Graph

You can use the Azure Active Directory PowerShell module version for Graph for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on. The cmdlets listed here are different from the MSOnline cmdlets which are part of Azure Active Directory Version 1.0.

The Azure AD PowerShell for Graph module has two versions: a Public Preview version and a General Availability (GA) version. It is not recommended to use the Public Preview version for production scenarios.

To download the modules from the PowerShell Gallery use the following;
- [AzureADPreview](https://www.powershellgallery.com/packages/AzureADPreview)
- [AzureAD](https://www.powershellgallery.com/packages/AzureAD)

## Azure Active Directory PowerShell for Graph release version history

For both Azure AD and Azure AD Preview modules, see the [Azure Active Directory PowerShell for Graph: Version release history](ad-pshell-v2-version-history.md).

## Installing the Azure AD Module

### Prerequisites

The Azure AD module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: 
- Windows 8.1
- Windows 8
- Windows 7
- Windows Server 2012 R2, 
- Windows Server 2012 
- Windows Server 2008 R2.

To install the General Availability version of the module, run:

```powershell
Install-Module AzureAD
```

To install the public preview release, run:

```powershell
Install-module AzureADPreview
```

Note that you cannot install both the preview version and the GA version on the same computer at the same time.

### About the PowerShell Gallery

The Azure AD module is distributed using the PowerShell gallery. Installing items from the Gallery requires the latest version of the PowerShellGet module, which is available in Windows 10, in Windows Management Framework (WMF) 5.0, or in the MSI-based installer (for PowerShell 3 and 4).
- [**Get Windows 10**](https://go.microsoft.com/fwlink/?LinkID=624830&clcid=0x409),
- [**Get WMF 5.0**](https://go.microsoft.com/fwlink/?LinkId=398175), or
- [**Get MSI Installer**](https://go.microsoft.com/fwlink/?LinkID=746217&clcid=0x409)


With the latest [PowerShellGet](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) module, you can:


+ Search through items in the Gallery with [**Find-Module**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Find-Script**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Save items to your system from the Gallery with [**Save-Module**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)    and [**Save-Script**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Install items from the Gallery with [**Install-Module**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Install-Script**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Upload items to the Gallery with [**Publish-Module**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Publish-Script**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Add your own custom repository with [**Register-PSRepository**](https://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)

Check out the [Getting Started](https://www.powershellgallery.com/) page for more information on how to use PowerShellGet commands with the Gallery. You can also run *Update-Help -Module PowerShellGet* to install local help for these commands.

### Supported Operating Systems

The **PowerShellGet** module requires **PowerShell 3.0 or newer**.

Therefore, **PowerShellGet** requires one of the following operating systems:

- Windows 10
- Windows 8.1 Pro
- Windows 8.1 Enterprise
- Windows 7 SP1
- Windows Server 2016 TP5
- Windows Server 2012 R2
- Windows Server 2008 R2 SP1

**PowerShellGet** also  requires .NET Framework 4.5 or above. You can install .NET Framework 4.5 or above from [here](https://msdn.microsoft.com/library/5a4x27ek.aspx).

## Updating the Azure AD Module

To check the version of the module installed on your computer run this command:

```PowerShell
Get-Module AzureADPreview

ModuleType Version Name                ExportedCommands
---------- ------- ----                ----------------
Binary     2.0.0.7 azureadpreview     {Add-AzureADAdmini...
```

To update the version of the Azure AD PowerShell module on your computer, re-run the **Install-Module** cmdlet:

```PowerShell
Install-Module AzureADPreview
```
This command checks the PowerShell gallery to see if a newer version is available. If yes, the newer than the one installed on your computer.

## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-AzureAD** at the Windows PowerShell command prompt. You will then be prompted for your credentials. If you want, you can supply your credentials in advance, for example:

```PowerShell
$AzureAdCred = Get-Credential
Connect-AzureAD -Credential $AzureAdCred
```

The first command prompts for credentials and stores them as $AzureAdCred.
The next command uses those credentials as $azureadcred to connect to the service.

To connect to a specific environment of Azure Active Directory, use the _AzureEnvironment_ parameter, as follows:

```PowerShell
Connect-AzureAD -AzureEnvironment "AzureGermanyCloud"
```

This example connects your PowerShell session to the German AzureAD environment.
See **Connect-AzureAD** for more information.

## Next steps

- See the [Azure Active Directory PowerShell for Graph module](../../azureadps-2.0/AzureAD/AzureActiveDirectory.md)
