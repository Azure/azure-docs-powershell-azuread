---
title: 'Azure AD PowerShell overview'
description: An introduction to the Azure AD PowerShell module.
ms.service: active-directory
ms.workload: identity
ms.topic: overview
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
---
# Azure Active Directory PowerShell for Graph

>[!NOTE]
> Azure AD PowerShell is planned for deprecation. See the [deprecation update](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/azure-ad-change-management-simplified/ba-p/2967456) for more details on the deprecation plans. We recommend that you start trying [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview). Microsoft Graph PowerShell is the replacement for Azure AD PowerShell and is recommended for interacting with Azure AD. See the [migration FAQ](migration-faq.yml) for answers to frequent migration queries.

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

