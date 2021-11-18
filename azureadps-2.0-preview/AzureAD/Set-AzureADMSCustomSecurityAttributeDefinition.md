---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSCustomSecurityAttributeDefinition

## SYNOPSIS
Updates an existing custom security attribute definition.

## SYNTAX

```
Set-AzureADMSCustomSecurityAttributeDefinition -Id <String> [-Description <String>] [-Status <String>]
 [-UsePreDefinedValuesOnly <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Updates an Azure Active Directory (Azure AD) custom security attribute definition object identified by ID.

## EXAMPLES

### Example 1
```powershell
Set-AzureADMSCustomSecurityAttributeDefinition -Id "Engineering_ProjectDate" -Description "Target completion date (YYYY/MM/DD)"
```

Update a custom security attribute definition.

- Attribute set: `Engineering`
- Attribute: `ProjectDate`

### Example 2
```powershell
Set-AzureADMSCustomSecurityAttributeDefinition -Id Engineering_Project -Status "Deprecated"
```

Deactivate a custom security attribute definition.

- Attribute set: `Engineering`
- Attribute: `Project`

## PARAMETERS

### -Description
Description of the custom security attribute definition.

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
The unique identifier of a custom security attribute definition in Azure AD.

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

### -Status
Specifies whether the custom security attribute is active or deactivated. Acceptable values are 'Available' and 'Deprecated'.

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

### -UsePreDefinedValuesOnly
Indicates whether only predefined values can be assigned to the custom security attribute.

```yaml
Type: Boolean
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
