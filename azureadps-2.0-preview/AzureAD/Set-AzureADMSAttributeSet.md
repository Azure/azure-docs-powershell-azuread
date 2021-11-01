---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSAttributeSet

## SYNOPSIS
Updates an existing attribute set.

## SYNTAX

```
Set-AzureADMSAttributeSet -Id <String> [-Description <String>] [-MaxAttributesPerSet <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Updates an Azure Active Directory (Azure AD) attribute set object identified by ID.

## EXAMPLES

### Example 1
```powershell
Set-AzureADMSAttributeSet -Id "Engineering" -Description "Attributes for cloud engineering team"
```

Update an attribute set

- Attribute set: `Engineering`

### Example 2
```powershell
Set-AzureADMSAttributeSet -Id "Engineering" -MaxAttributesPerSet 20
```

Update an attribute set

- Attribute set: `Engineering`

## PARAMETERS

### -Description
Description of the attribute set.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Name of the attribute set.

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

### -MaxAttributesPerSet
Maximum number of custom security attributes that can be defined in the attribute set.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
