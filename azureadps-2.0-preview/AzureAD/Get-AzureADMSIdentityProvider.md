---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSIdentityProvider

## SYNOPSIS
This cmdlet is used to retrieve the configured identity providers in the directory.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSIdentityProvider [<CommonParameters>]
```

### GetById
```
Get-AzureADMSIdentityProvider -Id <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to retrieve the identity providers that have been configured in the directory.
These identity providers can be used to allow users to sign up for or sign into applications secured by Azure AD B2C.

Configuring an identity provider in your Azure AD tenant also enables future B2B guest scenarios.
For example, an organization has resources in Office 365 that needs to be shared with a Gmail user.
The Gmail user will use their Google account credentials to authenticate and access the documents.

The current set of identity providers can be Microsoft, Google, Facebook, Amazon, or LinkedIn.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSIdentityProvider
```

This example retrieves the list of all configured identity providers and their properties.

### Example 2
```
PS C:\> Get-AzureADMSIdentityProvider -Id LinkedIn-OAUTH
```

This example retrieves the properties for the identity provider specified.

## PARAMETERS

### -Id
The unique identifier for an identity provider.

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

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
