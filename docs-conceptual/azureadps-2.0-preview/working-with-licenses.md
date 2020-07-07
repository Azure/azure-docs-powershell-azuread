---
services: active-directory
documentationcenter: ''

ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
---

# Working with licenses

(Get-AzureADUser).AssignedPlans gets you a list of assigned plans and their “capability status” – whether the particular service is Enabled or disabled based on the subscription status in commerce. The “Service” field is the type of the service behind the plan, and not the name of the service plan itself (the name is not included in this object at all, just the guid ID of the plan)

https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/assignedplan


Get-AzureADUserLicenseDetail gets you the information about product (SKU) licenses assigned to the user. Each product lists the service plans and their state. The state here is based on what the administrator did when assigning the license – did they Enable or Disable the specific service plan in the license?

https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/licensedetails

If your goal is to study the licenses assigned to users, you should only use Get-AzureADUserLicenseDetail.

If your goal is to see which services (Exchange, Sharepoint, etc.) are available to the user, and you do not care about specific licenses, then AssignedPlans is the way to go.
