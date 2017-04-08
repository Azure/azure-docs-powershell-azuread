# Azure ActiveDirectory (MSOnline)

You can use the Azure Active Directory Module for Windows PowerShell cmdlets for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.

Please note that we will begin to deprecate this module when the functionality of this module is migrated to the newer [Azure Active Directory PowerShell V2 Module](https://docs.microsoft.com/en-us/powershell/azuread/v2/azureactivedirectory). We advise customers who are creating new PowerShell scripts to use the newer module instead of this module.


## Install the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

The easiest way to install the module is from the [PowerShell Gallery](https://www.powershellgallery.com/packages/MSOnline). You can install the module with the Install-Module cmdlet:

  Install-Module MSOnline

You can also download the module from the [Azure Active Directory Connection download page](http://connect.microsoft.com/site1164/Downloads/DownloadDetails.aspx?DownloadID=59185), download its .msi file, and click **Run** to run the installer package.

## MSOnline Public Preview module

The MSOnline Public Preview release 1.1.130.0 is no longer available for download. If you are looking for the MSOL-Settings cmdlets to manage groups settings for Unified Groups, these are now available in the newer Azure AD PowerShell V2 Public Preview module, which can be found in the [Powershell Gallery for the Azure AD Preview module](https://www.powershellgallery.com/packages/AzureADPreview). You can install this module with the cmdlet

  Install-Module AzureADPreview
 
Note that the MSOL Settings cmdlets have been given a new name, more information about these cmdlets and how to use them can be found in [this article](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-accessmanagement-groups-settings-cmdlets).
 
**Important**

Effective October 20, 2014, the [Azure Active Directory Module for Windows PowerShell (32-bit version)](http://go.microsoft.com/fwlink/p/?linkid=236298) is discontinued.
Support for the 32-bit version will no longer occur, and future updates to the Azure Active Directory Module will be released only for the 64-bit version.

We strongly recommend you install the 64-bit version to ensure future support and compatibility.

You can also access previous versions of the Azure AD module from the [Microsoft Azure Active Directory PowerShell Module Version Release History](http://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) on the TechNet Wiki.


## Updating the Azure AD Module

You can run the **Get-Item** cmdlet to check the version of the DLL files of the module that you have currently installed:

```PowerShell
(Get-item C:\Windows\System32\WindowsPowerShell\v1.0\Modules\MSOnline\Microsoft.Online.Administration.Automation.PSModule.dll).VersionInfo.FileVersion
```

If the version number is lower than 1.0.8070.2, remove the existing version and re-install the module using the link in the previous section.
Use **Add/Remove Programs** in Control Panel to remove **Azure Active Directory Module for Windows PowerShell**, or if you have an older installation, to remove **Microsoft Online Services Module for Windows PowerShell**.
Uninstalling removes both the **MSOnline** and **MSOnlineExtended** modules.

The **Remove-Module** cmdlet removes the **MSOnline** cmdlets from the session but it does not uninstall the module.


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

See [Connect-MsolService](https://msdn.microsoft.com/en-us/library/azure/dn194123(v=azure.98).aspx) for more information.

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


## More about Windows PowerShell

Windows PowerShell is a task-based command-line shell and scripting language designed for system administration.
Unlike most shells, which accept and return text, Windows PowerShell is built on top of the .NET Framework, and accepts and returns .NET Framework objects.
Windows PowerShell introduces the concept of a cmdlet (pronounced "command-let"), a simple, single-function command-line tool built into the shell.
Cmdlets have the following naming convention: a verb and noun separated by a dash (-), such as Get-Help, Get-Process, and Start-Service.
Windows PowerShell includes more than one hundred basic core cmdlets.
For more information about Windows PowerShell, see [Getting Started with Windows PowerShell](https://msdn.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell).
