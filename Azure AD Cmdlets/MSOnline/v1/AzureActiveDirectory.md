---
Module Name: AzureActiveDirectory
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link: {{Please enter FwLink manually}}
Help Version: {{Please enter version of help manually (X.X.X.X) format}}
Locale: en-US
ms.assetid: BB86A603-6CD9-4299-89B8-30A2B4A011A0
---

# AzureActiveDirectory Module
## Description

You can use the Azure Active Directory Module for Windows PowerShell cmdlets for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.


## Install the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

There are two versions of the Azure Active Directory Module for Windows PowerShell available: a General Availability version and a Public Preview Version.
The Public Preview version contains cmdlets that have not yet been released for General Availability.

Select the version you want from the [Azure Active Directory Connection download page](http://connect.microsoft.com/site1164/Downloads/DownloadDetails.aspx?DownloadID=59185), download its .msi file, and click **Run** to run the installer package.

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


## AzureActiveDirectory Cmdlets
### [Add-MsolAdministrativeUnitMember](./Add-MsolAdministrativeUnitMember.md)
Adds a member to an administrative unit.


### [Add-MsolForeignGroupToRole](./Add-MsolForeignGroupToRole.md)
Adds a security group from a partner tenant to a Role in this tenant.


### [Add-MsolGroupMember](./Add-MsolGroupMember.md)
Adds a member to an existing security group.


### [Add-MsolRoleMember](./Add-MsolRoleMember.md)
Adds a member to an administrator role.


### [Add-MsolScopedRoleMember](./Add-MsolScopedRoleMember.md)
Adds a member to an administrative unit-scoped role.


### [Confirm-MsolDomain](./Confirm-MsolDomain.md)
Verifies a custom domain.


### [Confirm-MsolEmailVerifiedDomain](./Confirm-MsolEmailVerifiedDomain.md)



### [Connect-MsolService](./Connect-MsolService.md)
Initiates a connection to Azure Active Directory.


### [Convert-MsolDomainToFederated](./Convert-MsolDomainToFederated.md)
Converts the domain from using standard authentication to using single sign-on.


### [Convert-MsolDomainToStandard](./Convert-MsolDomainToStandard.md)
Converts the domain from using single sign-on (also known as identity federation) to using standard authentication.


### [Convert-MsolFederatedUser](./Convert-MsolFederatedUser.md)
Updates a user in a domain that was recently converted from single sign-on.


### [Disable-MsolDevice](./Disable-MsolDevice.md)
Disables a device object in Azure Active Directory.


### [Enable-MsolDevice](./Enable-MsolDevice.md)
Enables a device object in Azure Active Directory.


### [Get-MsolAccountSku](./Get-MsolAccountSku.md)
Returns all the SKUs for a company.


### [Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md)
Retrieves administrative units from Azure AD.


### [Get-MsolAdministrativeUnitMember](./Get-MsolAdministrativeUnitMember.md)
Gets members of an administrative unit.


### [Get-MsolAllSettings](./Get-MsolAllSettings.md)
Gets all directory settings object associated with tenant or group/user/service principal/application/device.


### [Get-MsolAllSettingTemplate](./Get-MsolAllSettingTemplate.md)
Gets all the directory setting templates that a tenant owns.


### [Get-MsolCompanyAllowedDataLocation](./Get-MsolCompanyAllowedDataLocation.md)
Get the current allowed data locations of a company from Azure Active Directory.


### [Get-MsolCompanyInformation](./Get-MsolCompanyInformation.md)
Retrieves company-level information.


### [Get-MsolContact](./Get-MsolContact.md)
Gets contacts from Azure Active Directory.


### [Get-MsolDeviceRegistrationServicePolicy](./Get-MsolDeviceRegistrationServicePolicy.md)
Gets the Azure Active Directory device registration service settings.


### [Get-MsolDevice](./Get-MsolDevice.md)
Gets an individual device, or a list of devices.


### [Get-MsolDirSyncConfiguration](./Get-MsolDirSyncConfiguration.md)



### [Get-MsolDirSyncFeatures](./Get-MsolDirSyncFeatures.md)
Gets the status of identity synchronization features for a tenant.


### [Get-MsolDirSyncProvisioningError](./Get-MsolDirSyncProvisioningError.md)
Checks for objects with synchronization provisioning errors in a tenant.


### [Get-MsolDomain](./Get-MsolDomain.md)
Retrieves a domain Microsoft Azure Active Directory.


### [Get-MsolDomainFederationSettings](./Get-MsolDomainFederationSettings.md)
Gets key settings for a federated domain.


### [Get-MsolDomainVerificationDns](./Get-MsolDomainVerificationDns.md)
Gets DNS records necessary to verify a domain.


### [Get-MsolFederationProperty](./Get-MsolFederationProperty.md)
Displays the properties of the Active Directory Federation Services 2.0 server and Microsoft Online.


### [Get-MsolGroup](./Get-MsolGroup.md)
Retrieves a group from Microsoft Azure Active Directory.


### [Get-MsolGroupMember](./Get-MsolGroupMember.md)
Retrieves all members of the specified group.


### [Get-MsolHasObjectsWithDirSyncProvisioningErrors](./Get-MsolHasObjectsWithDirSyncProvisioningErrors.md)



### [Get-MsolPartnerContract](./Get-MsolPartnerContract.md)
Gets a list of contracts for a partner.


### [Get-MsolPartnerInformation](./Get-MsolPartnerInformation.md)
Retrieves company-level information for partners.


### [Get-MsolPasswordPolicy](./Get-MsolPasswordPolicy.md)
Gets the current password policy for a tenant or a domain.


### [Get-MsolRole](./Get-MsolRole.md)
Gets administrator roles.


### [Get-MsolRoleMember](./Get-MsolRoleMember.md)
Gets members of a role.


### [Get-MsolScopedRoleMember](./Get-MsolScopedRoleMember.md)
Gets members of a role who are granted that role over an administrative unit.


### [Get-MsolServicePrincipal](./Get-MsolServicePrincipal.md)
Retrieves a service principal or list of service principals from Microsoft Azure Active Directory.


### [Get-MsolServicePrincipalCredential](./Get-MsolServicePrincipalCredential.md)
Gets credentials associated with a service principal.


### [Get-MsolSettings](./Get-MsolSettings.md)
Gets a directory setting.


### [Get-MsolSettingTemplate](./Get-MsolSettingTemplate.md)
Gets a directory setting template.


### [Get-MsolSubscription](./Get-MsolSubscription.md)
Gets subscriptions.


### [Get-MsolUser](./Get-MsolUser.md)
Gets users from Azure Active Directory.


### [Get-MsolUserByStrongAuthentication](./Get-MsolUserByStrongAuthentication.md)



### [Get-MsolUserRole](./Get-MsolUserRole.md)
Retrieves a list of roles that the specified user is a member of.


### [New-MsolAdministrativeUnit](./New-MsolAdministrativeUnit.md)
Adds a new administrative unit to Azure Active Directory.


### [New-MsolDomain](./New-MsolDomain.md)
Add a domain to Azure Active Directory.


### [New-MsolFederatedDomain](./New-MsolFederatedDomain.md)
Adds a new single sign-on domain to Microsoft Online Services and establishes the relying party trust.


### [New-MsolGroup](./New-MsolGroup.md)
Adds a new group to the Azure Active Directory.


### [New-MsolLicenseOptions](./New-MsolLicenseOptions.md)
Creates a License Options object.


### [New-MsolServicePrincipal](./New-MsolServicePrincipal.md)
Add a new service principal to the Microsoft Azure Active Directory.


### [New-MsolServicePrincipalAddresses](./New-MsolServicePrincipalAddresses.md)



### [New-MsolServicePrincipalCredential](./New-MsolServicePrincipalCredential.md)
Add a credential key to a service principal.


### [New-MsolSettings](./New-MsolSettings.md)
Creates a directory setting.


### [New-MsolUser](./New-MsolUser.md)
Creates a user in Azure Active Directory.


### [New-MsolWellKnownGroup](./New-MsolWellKnownGroup.md)



### [Redo-MsolProvisionContact](./Redo-MsolProvisionContact.md)
Retries the provisioning of a contact object in Azure Active Directory.


### [Redo-MsolProvisionGroup](./Redo-MsolProvisionGroup.md)
Retries the provisioning of a group object in Azure Active Directory.


### [Redo-MsolProvisionUser](./Redo-MsolProvisionUser.md)
Retries the provisioning of a user object in Azure Active Directory.


### [Remove-MsolAdministrativeUnit](./Remove-MsolAdministrativeUnit.md)
Deletes an administrative unit from Azure Active Directory.


### [Remove-MsolAdministrativeUnitMember](./Remove-MsolAdministrativeUnitMember.md)
Removes a member from an administrative unit.


### [Remove-MsolApplicationPassword](./Remove-MsolApplicationPassword.md)



### [Remove-MsolContact](./Remove-MsolContact.md)
Removes a contact from Azure Active Directory.


### [Remove-MsolDevice](./Remove-MsolDevice.md)
Remove a device object from Azure Active Directory.


### [Remove-MsolDomain](./Remove-MsolDomain.md)
Removes a domain from Azure Active Directory.


### [Remove-MsolFederatedDomain](./Remove-MsolFederatedDomain.md)
Removes a single sign-on domain from the domains in Microsoft Online.


### [Remove-MsolForeignGroupFromRole](./Remove-MsolForeignGroupFromRole.md)



### [Remove-MsolGroup](./Remove-MsolGroup.md)
Removes a group from Azure Active Directory.


### [Remove-MsolGroupMember](./Remove-MsolGroupMember.md)
Removes a member from a security group.


### [Remove-MsolRoleMember](./Remove-MsolRoleMember.md)
Removes a member from an administrator role.


### [Remove-MsolScopedRoleMember](./Remove-MsolScopedRoleMember.md)
Removes a user from an administrative unit-scoped role.


### [Remove-MsolServicePrincipal](./Remove-MsolServicePrincipal.md)
Removes a service principal from Azure Active Directory.


### [Remove-MsolServicePrincipalCredential](./Remove-MsolServicePrincipalCredential.md)
Removes a credential key from a service principal.


### [Remove-MsolSettings](./Remove-MsolSettings.md)
Removes a directory setting.


### [Remove-MsolUser](./Remove-MsolUser.md)
Removes a user from Microsoft Azure Active Directory.


### [Reset-MsolStrongAuthenticationMethodByUpn](./Reset-MsolStrongAuthenticationMethodByUpn.md)



### [Restore-MsolUser](./Restore-MsolUser.md)
Restores a deleted user.


### [Set-MsolADFSContext](./Set-MsolADFSContext.md)
Sets the context and credentials to connect to Microsoft Online and to the Active Directory Federation Services 2.0 server.


### [Set-MsolAdministrativeUnit](./Set-MsolAdministrativeUnit.md)
Updates the properties of an administrative unit.


### [Set-MsolCompanyAllowedDataLocation](./Set-MsolCompanyAllowedDataLocation.md)
Sets an allowed data location for a service type for a company in Azure Active Directory.


### [Set-MsolCompanyContactInformation](./Set-MsolCompanyContactInformation.md)
Sets company-level contact information.


### [Set-MsolCompanyMultiNationalEnabled](./Set-MsolCompanyMultiNationalEnabled.md)
Enables the multinational feature for a service type for a company with Azure Active Directory.


### [Set-MsolCompanySecurityComplianceContactInformation](./Set-MsolCompanySecurityComplianceContactInformation.md)



### [Set-MsolCompanySettings](./Set-MsolCompanySettings.md)
Sets company-level configuration settings.


### [Set-MsolDeviceRegistrationServicePolicy](./Set-MsolDeviceRegistrationServicePolicy.md)
Sets the Azure Active Directory device registration service settings.


### [Set-MsolDirSyncConfiguration](./Set-MsolDirSyncConfiguration.md)



### [Set-MsolDirSyncEnabled](./Set-MsolDirSyncEnabled.md)
Turns directory synchronization on or off for a company.


### [Set-MsolDirSyncFeature](./Set-MsolDirSyncFeature.md)
Sets identity synchronization features for a tenant.


### [Set-MsolDomain](./Set-MsolDomain.md)
Modifies settings of a domain.


### [Set-MsolDomainAuthentication](./Set-MsolDomainAuthentication.md)
Changes the authentication type of the domain.


### [Set-MsolDomainFederationSettings](./Set-MsolDomainFederationSettings.md)
Updates settings for a federated domain.


### [Set-MsolGroup](./Set-MsolGroup.md)
Updates a security group.


### [Set-MsolPartnerInformation](./Set-MsolPartnerInformation.md)
Sets company information for partners.


### [Set-MsolPasswordPolicy](./Set-MsolPasswordPolicy.md)
Updates the password policy of a specified domain or tenant.


### [Set-MsolServicePrincipal](./Set-MsolServicePrincipal.md)
Updates a service principal in Microsoft Azure Active Directory.


### [Set-MsolSettings](./Set-MsolSettings.md)
Updates a directory setting in Azure Active Directory.


### [Set-MsolUser](./Set-MsolUser.md)
Modifies a user in Azure Active Directory.


### [Set-MsolUserLicense](./Set-MsolUserLicense.md)
Updates the license assignment for a user.


### [Set-MsolUserPassword](./Set-MsolUserPassword.md)
Resets the password for a user.


### [Set-MsolUserPrincipalName](./Set-MsolUserPrincipalName.md)
Changes the user ID for a user.


### [Update-MsolFederatedDomain](./Update-MsolFederatedDomain.md)
Updates the settings in both the Active Directory Federation Services 2.0 server and Microsoft Online.

## Additional Resources

There are several other places you can get more information and help.
These include the following:

* [Azure Active Directory Forum](http://aka.ms/aadforum)
* [Azure AD Community Information Center](http://aka.ms/aadcommunity)
* [Azure Active Directory Community scripts](http://aka.ms/aadscripts)
* [Microsoft Azure Active Directory PowerShell Module Version Release History](http://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx)

## See Also

[Administering your Azure AD directory](https://msdn.microsoft.com/en-us/library/azure/hh967611(v=azure.98).aspx)

[Install Windows PowerShell for directory synchronization](https://msdn.microsoft.com/en-us/library/azure/jj151828(v=azure.98).aspx)
