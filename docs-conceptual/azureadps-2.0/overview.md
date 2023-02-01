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

>[!IMPORTANT]
> Azure AD Powershell is planned to be deprecated on June 30, 2023. For more details on the deprecation plans, see the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-azure-ad-blog/microsoft-entra-change-announcements-september-2022-train/ba-p/2967454). You can start trying [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview) to interact with Azure AD as you would in Azure AD PowerShell. In addition, Microsoft Graph PowerShell allows you access to all Microsoft Graph APIs and is available on PowerShell 7. For answers to frequent migration queries, see the [migration FAQ](migration-faq.yml).

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

