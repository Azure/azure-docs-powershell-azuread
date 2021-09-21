---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSCustomSecurityAttributeDefinition

## SYNOPSIS
Adds a new custom security attribute definition.

## SYNTAX

```
New-AzureADMSCustomSecurityAttributeDefinition -AttributeSet <String> [-Description <String>]
 -IsCollection <Boolean> -IsSearchable <Boolean> -Name <String> -Status <String> -Type <String>
 -UsePreDefinedValuesOnly <Boolean> [<CommonParameters>]
```

## DESCRIPTION
Adds a new AAzure Active Directory (Azure AD) custom security attribute definition object.

## EXAMPLES

### Example
```powershell
New-AzureADMSCustomSecurityAttributeDefinition -AttributeSet "TestSet" -Name "TestAttribute" -Description "TestAttributeDescription" -Type "String" -Status "Available" -IsCollection $true -IsSearchable $true -UsePreDefinedValuesOnly $true
```

Add a single definition

## PARAMETERS

### -AttributeSet
The unique identifier of an attribute set in Azure AD.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Description for the custom security attribute definition.

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

### -IsCollection
Determines whether the attribute is of collection type.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSearchable
Determines whether attribute values will be indexed for searching on objects which will be stamped with attribute values.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name that is unique within an attribute set.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Determines whether attribute is currently active or has been deprecated. Acceptable values are 'Available' and 'Deprecated'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specifies the data type of the attribute.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePreDefinedValuesOnly
Determines whether the attribute is free form or restricted to an allowed list of values only.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
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
