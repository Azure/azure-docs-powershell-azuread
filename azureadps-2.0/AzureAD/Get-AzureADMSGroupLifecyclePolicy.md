---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
ms.service: active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Get-AzureADMSGroupLifecyclePolicy

## SYNOPSIS
Retrieves the properties and relationships of a groupLifecyclePolicies object in Azure Active Directory.
If you specify no parameters, this cmdlet gets all groupLifecyclePolicies.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSGroupLifecyclePolicy [<CommonParameters>]
```

### GetById
```
Get-AzureADMSGroupLifecyclePolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSGroupLifecyclePolicy command retrieves the properties and relationships of a groupLifecyclePolicies object in Azure Active Directory.
If you specify no parameters, this cmdlet gets all groupLifecyclePolicies.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSGroupLifecyclePolicy
```

This command retrieves the group expiration settings configured for the tenant

## PARAMETERS

### -Id
Specifies the ID of a groupLifecyclePolicies object in Azure Active Directory

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

See the [migration guide for Get-AzureADMSGroupLifecyclePolicy](./migrate/Get-AzureADMSGroupLifecyclePolicy.md) to the Microsoft Graph PowerShell.

## INPUTS

### System.String
System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]

## OUTPUTS

### System.Object

## RELATED LINKS
