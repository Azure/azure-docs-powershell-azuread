# How can I install a previous version of a module?

> note: You need to be signed in with an administrator account on your computer to perform these actions

If you need to install a previous version of a module, you will first need to uninstall the current version (if one is installed already). You can do that with:

```powershell
Uninstall-Module -Name AzureAD
```

You can then install a previous version by specifying which version you want to install with the -RequiredVersion parameter, like in:

```powershell
Install-Module AzureAD -RequiredVersion 2.0.0.12
```

You can find all published version of the Azure AD PowerShell module in the module's PowerShell Gallery page by scrolling down to the bottom of the page.

> Note: If you want to install an older version of the Azure AD Preview module, you would use:

```powershell
Install-Module AzureADPreview -RequiredVersion 2.0.0.35
```