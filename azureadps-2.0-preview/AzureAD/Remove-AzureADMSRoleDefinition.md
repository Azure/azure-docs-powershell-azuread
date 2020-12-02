---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSRoleDefinition

## SYNOPSIS
Removes a role definition.

## SYNTAX

```
Remove-AzureADMSRoleDefinition -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADMSRoleDefinition cmdlet removes a role definition from Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-AzureADMSRoleDefinition -Id 62e90894-69f5-4237-9190-012177145e10
```

This command removes the specified role definition from AzureAD.

## PARAMETERS

### -Id
Spevifies the id for the role definition.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-AzureADMSRoleDefinition]()

[New-AzureADMSRoleDefinition]()

[Set-AzureADMSRoleDefinition]()