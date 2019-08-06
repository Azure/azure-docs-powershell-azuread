---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSRoleAssignment

## SYNOPSIS
Removes a role assignment.

## SYNTAX

```
Remove-AzureADMSRoleAssignment -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADMSRoleAssignment cmdlet removes a role assignment from Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-AzureADMSRoleAssignment -Id Y1vFBcN4i0e3ngdNDocmngJAWGnAbFVAnJQyBBLv1lM-1
```

Removes the specified role assignment from AzureAD.

## PARAMETERS

### -Id
Specifies the Id for role assignment.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-AzureADMSRoleAssignment]()

[New-AzureADMSRoleAssignment]()
