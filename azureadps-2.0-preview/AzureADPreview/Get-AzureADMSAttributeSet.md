---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSAttributeSet

## SYNOPSIS
Gets a list of attribute sets.

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
Gets a list of Azure Active Directory (Azure AD) attribute sets.

## EXAMPLES

### Example 1
```powershell
Get-AzureADMSAttributeSet
```

Get all attribute sets.

### Example 2
```powershell
Get-AzureADMSAttributeSet -Id "Engineering"
```

Get an attribute set.

- Attribute set: `Engineering`

## PARAMETERS

### -Id
The unique identifier of an Azure AD attribute set object.

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
