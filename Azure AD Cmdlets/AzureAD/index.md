# Azure Active Directory PowerShell for Graph

You can use the Azure Active Directory PowerShell for Graph Module for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on. The cmdlets listed here are different than the MSOL cmdlets which are part of the MSOnline module.

The Azure AD PowerShell PowerShell for Grpah module has two versions: a Public preview version and a General Availability version. It is not recommended to use the Public Preview version for production scenarios.


## Install the Azure AD PowerShell for Graph Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

The Azure AD PowerShell for Graph preview module can be downloaded from the PowerShell Gallery at the [AzureADPreview](https://www.powershellgallery.com/packages/AzureADPreview) page.

The Azure AD PowerShell for Graph General Availability module can be downloaded from the PowerShell Gallery at the [AzureAD](https://www.powershellgallery.com/packages/AzureAD) page. 

For instructions on how to install the module, see [The PowerShell Gallery](https://msdn.microsoft.com/powershell/gallery/readme).
Please ensure that you have followed these steps before installing the module on your computer.
You can also access previous versions of the Azure AD module from the Microsoft Azure Active Directory PowerShell Module Version Release History on the TechNet Wiki.


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

