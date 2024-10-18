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

# Remove-AzureADMSConditionalAccessPolicy

## SYNOPSIS
Deletes a conditional access policy in Azure Active Directory by Id.

## SYNTAX

```
Remove-AzureADMSConditionalAccessPolicy -PolicyId <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to delete a conditional access policy in Azure Active Directory by Id.
Conditional access policies are custom rules that define an access scenario.

## EXAMPLES

### Example 1: Deletes a conditional access policy in Azure AD by PolicyId.
```
PS C:\> Remove-AzureADMSConditionalAccessPolicy -PolicyId 1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5
```

This command deletes a conditional access policy in Azure AD.

## PARAMETERS

### -PolicyId
Specifies the policy id of a conditional access policy in Azure Active Directory.

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

## NOTES

See the [migration guide for Remove-AzureADMSConditionalAccessPolicy](./migrate/Remove-AzureADMSConditionalAccessPolicy.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS

[Get-AzureADMSConditionalAccessPolicy](Get-AzureADMSConditionalAccessPolicy.md)

[New-AzureADMSConditionalAccessPolicy](New-AzureADMSConditionalAccessPolicy.md)

[Set-AzureADMSConditionalAccessPolicy](Set-AzureADMSConditionalAccessPolicy.md)
