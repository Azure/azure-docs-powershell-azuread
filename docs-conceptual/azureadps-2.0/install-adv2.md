---
title: 'Install AzureAD PowerShell for Graph'
description: Installation guidance for the Azure AD PowerShell module.
ms.service: active-directory
ms.workload: identity
ms.topic: overview
ms.date: 12/16/2023
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
ms.reviewer: stevemutungi
---
# Install Azure Active Directory PowerShell for Graph

>[!IMPORTANT]
> Azure AD Powershell is planned for deprecation on **March 30, 2024**. For more details on the deprecation plans, see the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-azure-ad-blog/important-azure-ad-graph-retirement-and-powershell-module/ba-p/3848270). We encourage you to continue migrating to [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview), which is the recommended module for interacting with Azure AD. In addition, Microsoft Graph PowerShell allows you access to all Microsoft Graph APIs and is available on PowerShell 7. For answers to frequent migration queries, see the [Migration FAQ](migration-faq.yml).

You can use the Azure Active Directory PowerShell module version for Graph for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on. The cmdlets listed here are different from the MSOnline cmdlets which are part of Azure Active Directory PowerShell version 1.0.

The Azure AD PowerShell for Graph module has two versions: a Public Preview version and a General Availability (GA) version. It isn't recommended to use the Public Preview version for production scenarios.

Download the modules from the PowerShell Gallery use the following;
- [AzureADPreview](https://www.powershellgallery.com/packages/AzureADPreview)
- [AzureAD](https://www.powershellgallery.com/packages/AzureAD)

## Azure Active Directory PowerShell for Graph release version history

The release history for the Azure AD module and the Azure AD Preview module is here:[azure active directory powershell for graph: version release history](ad-pshell-v2-version-history.md).

## Installing the Azure AD Module

### Prerequisites

The Azure AD module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell:

:::row:::
    :::column:::
        - Windows 8.1
        - Windows 8
        - Windows 7
    :::column-end:::
    :::column:::
        - Windows Server 2012 R2, 
        - Windows Server 2012 
        - Windows Server 2008 R2.
    :::column-end:::
:::row-end:::

>[!Note]
> The Azure AD PowerShell module is not compatible with PowerShell 7. It is only supported in PowerShell 5.1.

To install the General Availability version of the module, run:

```powershell
Install-Module AzureAD
```

To install the public preview release, run:

```powershell
Install-module AzureADPreview
```

You cannot install both the preview version and the GA version on the same computer at the same time.

### About the PowerShell Gallery

The Azure AD module is distributed using the PowerShell Gallery. Installing items from the gallery requires the latest version of the PowerShellGet module, which is available in Windows 10, in Windows Management Framework (WMF) 5.0, or in the MSI-based installer (for PowerShell 3 and 4).
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

To update the version of the Azure AD PowerShell module on your computer, rerun the **Install-Module** cmdlet:

```PowerShell
Install-Module AzureADPreview
```
This command checks the PowerShell gallery to see if a newer version is available. If yes, the newer than the one installed on your computer.

## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-AzureAD** at the Windows PowerShell command prompt. You'll then be prompted for your credentials. If you want, you can supply your credentials in advance, for example:

```PowerShell
$AzureAdCred = Get-Credential
Connect-AzureAD -Credential $AzureAdCred
```

The first command prompts for credentials and stores them as $AzureAdCred.
The next command uses those credentials as $azureadcred to connect to the service.

> [!Note]
> The Azure AD and Azure AD Preview modules comprise of cmdlets with different naming conventions i.e. `-AzureAD` and `-AzureADMS`. The `-AzureAD` cmdlets connect to the Azure AD Graph endpoint `https://graph.windows.net` while the `-AzureADMS` cmdlets make calls to the Microsoft Graph endpoint `graph.microsoft.com`. Authentication is handled silently when you change the calls from one endpoint to another and you are not prompted for the credentials again.

To connect to a specific environment of Azure Active Directory, use the _AzureEnvironment_ parameter, as follows:

```PowerShell
Connect-AzureAD -AzureEnvironment "AzureGermanyCloud"
```

This example connects your PowerShell session to the German AzureAD environment.
See **Connect-AzureAD** for more information.

## Next steps

- See the [New features and improvements](ad-pshell-v2-version-history.md).