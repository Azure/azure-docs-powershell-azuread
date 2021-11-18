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
Adds a new Azure Active Directory (Azure AD) custom security attribute definition object.

## EXAMPLES

### Example
```powershell
New-AzureADMSCustomSecurityAttributeDefinition -AttributeSet "Engineering" -Name "ProjectDate" -Description "Target completion date" -Type "String" -Status "Available" -IsCollection $false -IsSearchable $true -UsePreDefinedValuesOnly $true
```

Add a custom security attribute definition.

- Attribute set: `Engineering`
- Attribute: `ProjectDate`
- Attribute data type: String

## PARAMETERS

### -AttributeSet
Name of the attribute set in Azure AD.

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
Indicates whether multiple values can be assigned to the custom security attribute.

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
Indicates whether custom security attribute values will be indexed for searching on objects that are assigned attribute values.

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
Name of the custom security attribute. Must be unique within an attribute set.

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
Specifies whether the custom security attribute is active or deactivated. Acceptable values are 'Available' and 'Deprecated'.

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
Indicates whether only predefined values can be assigned to the custom security attribute. If set to false, free-form values are allowed.

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
