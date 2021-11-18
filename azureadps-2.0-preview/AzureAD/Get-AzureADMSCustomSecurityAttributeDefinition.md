---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSCustomSecurityAttributeDefinition

## SYNOPSIS
Gets a list of custom security attribute definitions.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSCustomSecurityAttributeDefinition [<CommonParameters>]
```

### GetById
```
Get-AzureADMSCustomSecurityAttributeDefinition -Id <String> [<CommonParameters>]
```

## DESCRIPTION
Gets a list of Azure Active Directory (Azure AD) custom security attribute definitions.

## EXAMPLES

### Example 1
```powershell
Get-AzureADMSCustomSecurityAttributeDefinition
```

Get all custom security attribute definitions.

### Example 2
```powershell
Get-AzureADMSCustomSecurityAttributeDefinition -Id "Engineering_ProjectDate" 
```

Get a custom security attribute definition.

- Attribute set: `Engineering`
- Attribute: `ProjectDate`

## PARAMETERS

### -Id
The unique identifier of an Azure AD custom security attribute definition object.

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
