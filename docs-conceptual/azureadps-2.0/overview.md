---
title: 'Azure AD PowerShell overview'
description: An introduction to the Azure AD PowerShell module.
ms.service: active-directory
ms.workload: identity
ms.topic: overview
ms.date: 07/10/2017
ms.author: eunicewaweru
ms.custom: posh-docs-conceptual
---

# Azure Active Directory PowerShell for Graph

>[!IMPORTANT]
>Azure AD and MSOnline PowerShell are now deprecated as of March 30, 2024. To learn more, read the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-blog/important-update-deprecation-of-azure-ad-powershell-and-msonline/ba-p/4094536). The only support offered for these PowerShell modules after deprecation will be support in migrating to Microsoft Graph PowerShell SDK and security fixes. Once these modules are deprecated, they continue to work for a minimum of six (6) months before being retired.
>We recommend migrating to [Microsoft Graph PowerShell](https://learn.microsoft.com/powershell/microsoftgraph/overview) to interact with Microsoft Entra ID (formerly Azure AD). Microsoft Graph PowerShell allows access to all Microsoft Graph APIs and is available on PowerShell 7. For answers to common migration queries, see the [Migration FAQ](https://learn.microsoft.com/powershell/azure/active-directory/migration-faq).

Azure Active Directory PowerShell for Graph (Azure AD PowerShell) is a module IT Pros commonly use to manage their Azure Active Directory. The cmdlets in the Azure AD PowerShell module enable you to retrieve data from the directory, create new objects in the directory, update existing objects, remove objects, as well as configure the directory and its features.

For more information about, or for the syntax of, any of the cmdlets, use the `Get-Help <cmdlet name>` command, where `<cmdlet name>` is the name of the cmdlet that you want to research.
For more detailed information, you can run any of the following commands:

* `Get-Help <cmdlet name> -Detailed`
* `Get-Help <cmdlet name> -Examples`
* `Get-Help <cmdlet name> -Full`

If you are developing new PowerShell scripts with Azure AD cmdlets we advise you to use the newer [Azure Active Directory PowerShell for Graph cmdlets](/powershell/module/azuread?view=azureadps-2.0&preserve-view=true). 

Refer to the modules below for a full list of cmdlets and their functionality.

Module | Description
------ | -----------
[AzureAD](/powershell/module/azuread?view=azureadps-2.0&preserve-view=true) | Azure Active Directory PowerShell for Graph
[MSOnline](/powershell/module/msonline?view=azureadps-1.0&preserve-view=true)| MSOnline PowerShell
[Microsoft Graph PowerShell](/powershell/microsoftgraph/overview?view=graph-powershell-1.0&preserve-view=true) (Recommended)| Microsoft Graph PowerShell


