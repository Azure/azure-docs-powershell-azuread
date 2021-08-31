---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSAttributeSet

## SYNOPSIS
Get a list of Azure Active Directory AttributeSets.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSAttributeSet [<CommonParameters>]
```

### GetById
```
Get-AzureADMSAttributeSet -Id <String> [<CommonParameters>]
```

## DESCRIPTION
Get a list of Azure Active Directory AttributeSets.

## EXAMPLES

### Example 1
```powershell
Get-AzureADMSAttributeSet
```

Get all AttributeSets

### Example 2
```powershell
Get-AzureADMSAttributeSet -Id "testAttributeSet"
```

Get single AttributeSet

## PARAMETERS

### -Id
The unique identifier of an Azure Active Directory AttributeSet object.

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

## INPUTS

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
