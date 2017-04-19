# How can I find the version of the Azure AD PowerShell module I'm using?

To find the version of the Azure AD PowerShell module you have installed on your computer, you can use the command:

```powershell
Import-Module AzureAD
Get-Module -Name AzureAD
```

This command will return the version of the Azure AD Module that is installed on your computer, like this:

```powershell
ModuleType Version    Name                                ExportedCommands
---------- -------    ----                                ----------------
Binary     2.0.0.109  AzureAD                             {Add-AzureADApplic...
```

> Note: If you are using the Azure AD preview module, you should use:

```powershell
Import-Module AzureADPreview
Get-Module -Name AzureADPreview
```