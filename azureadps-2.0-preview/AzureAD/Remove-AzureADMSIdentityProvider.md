---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSIdentityProvider

## SYNOPSIS
This cmdlet is used to delete an identity provider in the directory.

## SYNTAX

```
Remove-AzureADMSIdentityProvider -Id <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to delete an identity provider that has been configured in the directory.
The identity provider will be permanently deleted.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADMSIdentityProvider -Id LinkedIn-OAUTH
```

This example removes the specified identity provider.

## PARAMETERS

### -Id
The unique identifier for an identity provider.

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
