---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMScustomSecurityAttributeDefinitionAllowedValues

## SYNOPSIS
Adds an allowed value for a custom security attribute definition.

## SYNTAX

```
Add-AzureADMScustomSecurityAttributeDefinitionAllowedValues -CustomSecurityAttributeDefinitionId <String>
 -Id <String> -IsActive <Boolean> [<CommonParameters>]
```

## DESCRIPTION
Adds an allowed value for a Azure Active Directory (Azure AD) custom security attribute definition.

## EXAMPLES

### Example
```powershell
Add-AzureADMScustomSecurityAttributeDefinitionAllowedValues -CustomSecurityAttributeDefinitionId TestSet_TestAttribute -Id "TestAllowedValue" -IsActive $true
```

Add a single allowed value

## PARAMETERS

### -CustomSecurityAttributeDefinitionId
The unique identifier of a CustomSecurityAttributeDefinition in Azure AD.

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
The unique identifier of an object in Azure AD.

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

### -IsActive
Determines whether the allowed value is active or not, if set to false, this value cannot be stamped on any other principal/resource.

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

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
