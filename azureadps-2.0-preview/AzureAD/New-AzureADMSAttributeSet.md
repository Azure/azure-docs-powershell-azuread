---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSAttributeSet

## SYNOPSIS
Create a new Azure Active Directory AttributeSet.

## SYNTAX

```
New-AzureADMSAttributeSet [-Id <String>] [-Description <String>] [-MaxAttributesPerSet <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Create a new Azure Active Directory AttributeSet object.

## EXAMPLES

### Example 1
```powershell
New-AzureADMSAttributeSet -Id "testAttributeSet" -Description "TestAttributeDescription" -MaxAttributesPerSet 10
```

Post single AttributeSet

## PARAMETERS

### -Description
Description for the attribute set.

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
String identifier that is unique within a tenant.

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

### -MaxAttributesPerSet
Number of attributes that can be added in the given set.

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

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
