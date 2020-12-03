---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADTrustedCertificateAuthority

## SYNOPSIS
Gets the trusted certificate authority.

## SYNTAX

```
Get-AzureADTrustedCertificateAuthority [-TrustedIssuer <String>] [-TrustedIssuerSki <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADTrustedCertificateAuthority cmdlet gets the trusted certificate authority in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve the trusted certificate authorities that are defined in your directory
```
PS C:\> Get-AzureADTrustedCertificateAuthority
```

This command retrieve the trusted certificate authorities that are defined in your directory.

### Example 2: Retrieve the trusted certificate authorities that are defined in your directory based on TrustedIssuer
```
PS C:\> Get-AzureADTrustedCertificateAuthority -TrustedIssuer "CN=example.azure.com, O=MSIT. Ltd, L=Redmond, C=US"
```

This command retrieve the trusted certificate authorities that are defined in your directory based on TrustedIssuer.

### Example 3: Retrieve the trusted certificate authorities that are defined in your directory based on TrustedIssuerSki
```
PS C:\> Get-AzureADTrustedCertificateAuthority -TrustedIssuerSki 4BA2D7AC2A5DF47C70E19E61EDFB4E62B3BF67FD
```

This command retrieve the trusted certificate authorities that are defined in your directory based on TrustedIssuerSki.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedIssuer
Specifies a trusted issuer.

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

### -TrustedIssuerSki
@{Text=}

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

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADTrustedCertificateAuthority]()

[Remove-AzureADTrustedCertificateAuthority]()

[Set-AzureADTrustedCertificateAuthority]()

[Online help and examples for working with certificate authority](https://azure.microsoft.com/en-us/documentation/articles/active-directory-certificate-based-authentication-ios/)

