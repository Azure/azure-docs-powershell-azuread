---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSAttributeSet

## SYNOPSIS
Update an existing Azure Active Directory AttributeSet.

## SYNTAX

```
Set-AzureADMSAttributeSet -Id <String> [-Description <String>] [-MaxAttributesPerSet <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Updates an Azure Active Directory AttributeSet object identified by id.

## EXAMPLES

### Example 1
```powershell
Set-AzureADMSAttributeSet -Id "testAttributeSet" -Description "New Test Description"
```

Patch single AttributeSet

### Example 2
```powershell
Set-AzureADMSAttributeSet -Id "testAttributeSet" -MaxAttributesPerSet 20
```

Patch single AttributeSet

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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
