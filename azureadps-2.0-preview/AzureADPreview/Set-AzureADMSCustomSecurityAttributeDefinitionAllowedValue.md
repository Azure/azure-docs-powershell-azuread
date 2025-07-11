---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSCustomSecurityAttributeDefinitionAllowedValue

## SYNOPSIS
Updates an existing custom security attribute definition predefined value.

## SYNTAX

```
Set-AzureADMSCustomSecurityAttributeDefinitionAllowedValue -CustomSecurityAttributeDefinitionId <String>
 -Id <String> [-IsActive <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Updates an Azure Active Directory (Azure AD) custom security attribute definition predefined value object identified by ID.

## EXAMPLES

### Example
```powershell
Set-AzureADMSCustomSecurityAttributeDefinitionAllowedValue -CustomSecurityAttributeDefinitionId "Engineering_Project" -Id "Alpine" -IsActive $false
```

Deactivate a predefined value.

- Attribute set: `Engineering`
- Attribute: `Project`
- Predefined value: `Alpine`

## PARAMETERS

### -CustomSecurityAttributeDefinitionId
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

### -Id
Predefined value for the custom security attribute.

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

### -IsActive
Specifies whether the predefined value is active or deactivated. If set to false, this predefined value cannot be assigned to any additional supported directory objects.

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
