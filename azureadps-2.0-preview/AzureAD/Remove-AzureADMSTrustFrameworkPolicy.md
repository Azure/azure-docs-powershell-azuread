---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Remove-AzureADMSTrustFrameworkPolicy

## SYNOPSIS
This cmdlet is used to delete a trust framework policy (custom policy) in the directory.

## SYNTAX

```
Remove-AzureADMSTrustFrameworkPolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to delete a trust framework policy in the directory.
The trust framework policy will be permanently deleted.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin
```

This example removes the specified trust framework policy.

## PARAMETERS

### -Id
The unique identifier for a trust framework policy.

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
