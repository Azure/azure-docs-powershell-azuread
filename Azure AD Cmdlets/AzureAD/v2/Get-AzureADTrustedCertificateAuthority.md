---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 48304207-E7EC-4436-A15C-C9F428E8E98C
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
The **Get-AzureADTrustedCertificateAuthority** cmdlet gets the trusted certificate authority in Azure Active Directory (AD).

## PARAMETERS

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

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[New-AzureADTrustedCertificateAuthority](./New-AzureADTrustedCertificateAuthority.md)

[Remove-AzureADTrustedCertificateAuthority](./Remove-AzureADTrustedCertificateAuthority.md)

[Set-AzureADTrustedCertificateAuthority](./Set-AzureADTrustedCertificateAuthority.md)

