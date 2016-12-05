---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: 51B0B9EC-8A74-4C48-A6CE-2FA005A0B3F0
online version: 
schema: 2.0.0
---

# Remove-AzureADTrustedCertificateAuthority

## SYNOPSIS
Removes a trusted certificate authority.

## SYNTAX

```
Remove-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation <CertificateAuthorityInformation>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADTrustedCertificateAuthority** cmdlet removes a trusted certificate authority from Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -CertificateAuthorityInformation
```yaml
Type: CertificateAuthorityInformation
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureADTrustedCertificateAuthority](./Get-AzureADTrustedCertificateAuthority.md)

[New-AzureADTrustedCertificateAuthority](./New-AzureADTrustedCertificateAuthority.md)

[Set-AzureADTrustedCertificateAuthority](./Set-AzureADTrustedCertificateAuthority.md)
