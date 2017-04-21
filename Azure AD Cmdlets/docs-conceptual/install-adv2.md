# Azure Active Directory PowerShell Version 2

You can use the Azure Active Directory PowerShell Module Version 2 for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on. The cmdlets listed here are different than the MSOL cmdlets which are part of Azure Active Directory Version 1.0.

The Azure AD PowerShell Version 2 module has two versions: a Public preview version and a General Availability version. It is not recommended to use the Public Preview version for production scenarios.
The Azure AD PowerShell Version 2 preview module can be downloaded from the PowerShell Gallery at the [AzureADPreview](https://www.powershellgallery.com/packages/AzureADPreview) page.
The Azure AD PowerShell Version 2 General Availability module can be downloaded from the PowerShell Gallery at the [AzureAD](https://www.powershellgallery.com/packages/AzureAD) page. 

## Installing the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

If your computer has all the prerequisites for the installation, to install the General Availability version of the module on your computer you can run

```powershell
Install-Module AzureAD
```

To install the public preview release, use

```powershell
Install-module AzureADPreview
```

Note that you cannot install both the preview version and the GA version on the same computer at the same time.

### About the PowerShell Gallery
The Azure AD module is distributed using the PowerShell gallery. Installing items from the Gallery requires the latest version of the PowerShellGet module, which is available in Windows 10, in Windows Management Framework (WMF) 5.0, or in the MSI-based installer (for PowerShell 3 and 4).
- [**Get Windows 10**](http://go.microsoft.com/fwlink/?LinkID=624830&clcid=0x409),
- [**Get WMF 5.0**](http://go.microsoft.com/fwlink/?LinkId=398175), or
- [**Get MSI Installer**](http://go.microsoft.com/fwlink/?LinkID=746217&clcid=0x409)

With the latest[PowerShellGet](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)module, you can:

+ Search through items in the Gallery with [**Find-Module**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Find-Script**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Save items to your system from the Gallery with [**Save-Module**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)    and [**Save-Script**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Install items from the Gallery with [**Install-Module**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Install-Script**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Upload items to the Gallery with [**Publish-Module**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409) and [**Publish-Script**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)
+ Add your own custom repository with [**Register-PSRepository**](http://go.microsoft.com/fwlink/?LinkID=760387&clcid=0x409)

Check out the [Getting Started](psgallery/psgallery_gettingstarted.md) page for more information on how to use PowerShellGet commands with the Gallery. You can also run *Update-Help -Module PowerShellGet* to install local help for these commands.

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

**PowerShellGet** also  requires .NET Framework 4.5 or above. You can install .NET Framework 4.5 or above from [here](https://msdn.microsoft.com/en-us/library/5a4x27ek.aspx).

## Updating the Azure AD Module

You can check the version of the module you have installed on your computer by running this command:

```PowerShell
PS C:\WINDOWS\system32> Get-Module AzureADPreview

ModuleType Version Name                ExportedCommands
---------- ------- ----                ----------------
Binary     2.0.0.7 azureadpreview     {Add-AzureADAdmini...
```

To update the version of the Azure AD PowerShell module on your computer, re-run the **Install-Module** cmdlet:

```PowerShell
PS C:\WINDOWS\system32> Install-Module AzureADPreview
```
This command checks the PowerShell gallery to see if a newer version is available and installs it on your computer if the version on the PowerShell Gallery is newer than the one installed on your computer.

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


## More about Windows PowerShell

Windows PowerShell is a task-based command-line shell and scripting language designed for system administration.
Unlike most shells, which accept and return text, Windows PowerShell is built on top of the .NET Framework, and accepts and returns .NET Framework objects.

Windows PowerShell introduces the concept of a cmdlet (pronounced "command-let"), a simple, single-function command-line tool built into the shell.
Cmdlets have the following naming convention: a verb and noun separated by a dash (-), such as **Get-Help**, **Get-Process**, and **Start-Service**.
Windows PowerShell includes more than one hundred basic core cmdlets.

For more information about, or for the syntax of, any of the cmdlets, use the `Get-Help <cmdlet name>` command, where `<cmdlet name>` is the name of the cmdlet that you want to research.
For more detailed information, you can run any of the following commands:

* `Get-Help <cmdlet name> -Detailed`
* `Get-Help <cmdlet name> -Examples`
* `Get-Help <cmdlet name> -Full`

For more information about Windows PowerShell, see the [Getting Started with Windows PowerShell](https://msdn.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell).

