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
# I'm looking for a user or a group but PowerShell does not return the object
Sometimes you are trying to find an object, for instance a group or a user, but PowerShell does not return the object you are looking for. However, you are sure it exists, perhaps because it shows up in the portal, or perhaps because you just created it yourself. 
What is happening here and how can we fix this?

## Searching for objects
The most common way to search for a user is to use Get-AzureADUser - which returns all users in your directory - and then filter on the property values you are looking for, e.g.

```powershell
Get-AzureADUser | Where ($_.City -eq "London")
```

You would expect PowerShell to return all users where the value for the City property equals London. However... the Get-AzureADUser cmdlet by default only returns the first 100 objects it finds, and the subsequent Where cmdlet filters these first 100 objects to find users where the City equals London. If the user you are looking for exists in your directory but is not in the first 100 users that are returned by the Get-azureADUser cmdlet, that user will not be returned.

# How to return all objects for subsequent filtering
To get the Get-AzureADUser cmdlet to return all users, you would use the -All parameter, as in

```powershell
Get-AzureADUser -All $True
```

Now all user objects are returned, and the filter works on all user objects in your directory. So the correct way to find all users where City equals London is:

```powershell
Get-AzureADUser -All $True | Where ($_.City -eq "London")
```

Note that this approach works for all properties of objects. For a limited number of string properties you can also use the -SearchString parameter, as in

```powershell
Get-AzureADUser -SearchString "London"
```
This will return all users where one of the qualifying string attributes on the user object equals "London" - which would include users who's DisplayName equals "Jack London" or whre the Department equals "London".
