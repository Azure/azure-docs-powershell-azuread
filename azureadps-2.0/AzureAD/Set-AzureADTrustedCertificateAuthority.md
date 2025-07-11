---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADTrustedCertificateAuthority

## SYNOPSIS
Updates a trusted certificate authority.

## SYNTAX

```
Set-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation <CertificateAuthorityInformation>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADTrustedCertificateAuthority cmdlet updates a trusted certificate authority in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Updates the trusted certificate authorities that are defined in your directory
```
PS C:\> $cer = Get-AzureADTrustedCertificateAuthority #Get the CertificateAuthorityInformation object
PS C:\> $cer[0].CrlDistributionPoint = "https://example.crl"
PS C:\> Set-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation $cer[0]
```

This command updates the trusted certificate authorities that are defined in your directory.

## PARAMETERS

### -CertificateAuthorityInformation
Specifies a CertificateAuthorityInformation object.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADTrustedCertificateAuthority](Get-AzureADTrustedCertificateAuthority.md)

[New-AzureADTrustedCertificateAuthority](New-AzureADTrustedCertificateAuthority.md)

[Remove-AzureADTrustedCertificateAuthority](Remove-AzureADTrustedCertificateAuthority.md)

