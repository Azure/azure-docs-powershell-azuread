---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
ms.service: azure-active-directory
ms.topic: reference
ms.date: 01/19/2024
ms.author: eunicewaweru
manager: CelesteDG
author: msewaweru
ms.reviewer: stevemutungi
---

# Remove-AzureADMSGroupLifecyclePolicy

## SYNOPSIS
Deletes a groupLifecyclePolicies object

## SYNTAX

```
Remove-AzureADMSGroupLifecyclePolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADMSGroupLifecyclePolicy command deletes a groupLifecyclePolicies object in Azure Active Directory.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADMSGroupLifecyclePolicy -Id "13bed58e-6144-41e5-abbd-47c95964e671"
```

This cmdlet deletes the groupLifecyclePolicies object that has the specified ID.

## PARAMETERS

### -Id
Specifies the ID of the groupLifecyclePolicies object that this cmdlet removes.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object

## NOTES

See the [migration guide for Remove-AzureADMSGroupLifecyclePolicy](./migrate/Remove-AzureADMSGroupLifecyclePolicy.md) to the Microsoft Graph PowerShell.

## RELATED LINKS
