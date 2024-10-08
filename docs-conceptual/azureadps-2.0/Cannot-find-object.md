---
services: active-directory
documentationcenter: ''
title: 'Cannot find object'
description: This article provides guidance on how to filter data returned by a cmdlet.
ms.service: azure-active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 02/11/2022
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
---
# I'm looking for a user or a group but PowerShell does not return the object

Sometimes you're trying to find an object--for instance, a group or a user--but PowerShell doesn't return the object you're looking for. However, you're sure it exists because it shows up in the portal or because you just created the object.
What is happening here and how can you fix this?

## Searching for objects

The most common way to search for a user is to use Get-AzureADUser to get all users in your directory and then filter on the property values that you're looking for. For example:

```powershell
Get-AzureADUser | Where {$_.City -eq "London"}
```

You would expect PowerShell to return all users where the value for the City property equals `London`. However, the Get-AzureADUser cmdlet by default only returns the first 100 objects it finds. The subsequent `where` filters these first 100 objects to find users where the City equals `London`. If the user you're looking for exists in your directory but is not in the first 100 users that are returned by the Get-azureADUser cmdlet, that user will not be returned.

## How to return all objects for subsequent filtering

To get the Get-AzureADUser cmdlet to return all users, use the `-All` parameter. For example:

```powershell
Get-AzureADUser -All $True
```

Now, all user objects are returned, and the filter works on all user objects in your directory. So, the correct way to find all users where City equals London is:

```powershell
Get-AzureADUser -All $True | Where {$_.City -eq "London"}
```

This approach works for all properties of objects. For a limited number of string properties, you can also use the `-SearchString` parameter. For example:

```powershell
Get-AzureADUser -SearchString "London"
```

This will return all users where one of the qualifying string attributes on the user object equals `London`, which would include users whose DisplayName equals `Jack London` or where the Department equals `London`.
