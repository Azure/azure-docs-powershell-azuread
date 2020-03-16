---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADDomain

## SYNOPSIS
Removes a domain.

## SYNTAX

```
Remove-AzureADDomain -Name <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADDomain cmdlet removes a domain from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove a domain
```
PS C:\>Remove-AzureADDomain -Name Contoso.com
```

This command removes a domain.

## PARAMETERS

### -Name
Specifies the name of the domain to remove.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Confirm-AzureADDomain]()

[Get-AzureADDomain]()

[New-AzureADDomain]()

[Set-AzureADDomain]()

