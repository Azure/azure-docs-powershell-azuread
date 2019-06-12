---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-AzureADMSTrustFrameworkPolicy

## SYNOPSIS
This cmdlet is used to retrieve the created trust framework policies (custom policies) in the directory.

## SYNTAX

```
Get-AzureADMSTrustFrameworkPolicy -Id <String> [-OutputFilePath <String>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to retrieve the trust framework policies that have been created in the directory.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSTrustFrameworkPolicy
```

This example retrieves the list of all trust framework policies in the directory.

### Example 2
```
PS C:\> Get-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin
```

This example retrieves the contents of the specified trust framework policy.

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

### -OutputFilePath
@{Description=System.Management.Automation.PSObject\[\]}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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
