---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSRoleAssignment

## SYNOPSIS
Removes an Azure AD role assignment.

## SYNTAX

```
Remove-AzureADMSRoleAssignment -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADMSRoleAssignment cmdlet removes a role assignment from Azure Active Directory (Azure AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-AzureADMSRoleAssignment -Id Y1vFBcN4i0e3ngdNDocmngJAWGnAbFVAnJQyBBLv1lM-1
```

Removes the specified role assignment from Azure AD.

## PARAMETERS

### -Id
Specifies the ID for role assignment.

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

### string
## OUTPUTS

## NOTES

## RELATED LINKS
