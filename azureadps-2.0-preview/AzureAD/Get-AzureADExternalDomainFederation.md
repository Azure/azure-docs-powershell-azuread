---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADExternalDomainFederation

## SYNOPSIS
Get an externalDomainFederation by external domain name.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADExternalDomainFederation [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADExternalDomainFederation -ExternalDomainName <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Gets an external domain federation setting for a given external domain.
```
Get-AzureADExternalFederationDomain -ExternalDomainName "test.com"
```

This command gets an external domain federation setting.

## PARAMETERS

### -ExternalDomainName
The unique identifer of an externalDomainFederation in Azure Active Directory

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

### -All
Boolean to express that return all results from the server for the specific query

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
The maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
The oData v3.0 filter statement. 
Controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
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

## OUTPUTS

## NOTES

## RELATED LINKS
