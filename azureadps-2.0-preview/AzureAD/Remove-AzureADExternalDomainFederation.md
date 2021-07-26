---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADExternalDomainFederation

## SYNOPSIS
Delete an externalDomainFederation by external domain name.

## SYNTAX

```
Remove-AzureADExternalDomainFederation -ExternalDomainName <String> [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Deletes an external domain federation setting for a given external domain.
```
Remove-AzureADExternalFederationDomain -ExternalDomainName "test.com"
```

This command deletes an external domain federation setting.

## PARAMETERS

### -ExternalDomainName
The unique identifer of an externalDomainFederation in Azure Active Directory

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
