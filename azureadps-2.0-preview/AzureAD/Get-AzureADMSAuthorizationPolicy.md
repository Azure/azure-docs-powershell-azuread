---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: azureadpreview
online version:
schema: 2.0.0
---

# Get-AzureADMSAuthorizationPolicy

## SYNOPSIS
Gets an authorization policy.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSAuthorizationPolicy [<CommonParameters>]
```

### GetById
```
Get-AzureADMSAuthorizationPolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSAuthorizationPolicy cmdlet gets an Azure Active Directory authorization policy.

## EXAMPLES

### Example 1: Get an authorization policy by ID
```
PS C:\>Get-AzureADMSAuthorizationPolicy -Id "authorizationPolicy"
```

## PARAMETERS

### -Id
Specifies the unique identifier of the authorization policy.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-AzureADMSAuthorizationPolicy]()

