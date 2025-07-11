---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADTrustedCertificateAuthority

## SYNOPSIS
Creates a trusted certificate authority.

## SYNTAX

```
New-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation <CertificateAuthorityInformation>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADTrustedCertificateAuthority cmdlet creates a trusted certificate authority in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Creates the trusted certificate authorities in your directory
```
PS C:\> $new_ca = New-Object -TypeName Microsoft.Open.AzureAD.Model.CertificateAuthorityInformation #Create CertificateAuthorityInformation object
		PS C:\> $new_ca.AuthorityType = "RootAuthority"
		PS C:\> $new_ca.CrlDistributionPoint = "https://example.crl"
		PS C:\> $new_ca.DeltaCrlDistributionPoint = "https://deltaexample.crl"
		PS C:\> $new_ca.TrustedCertificate = "Path to .cer file(including cer file name)"
		PS C:\> New-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation $new_ca
```

This command creates the trusted certificate authorities in your directory.

## PARAMETERS

### -CertificateAuthorityInformation
@{Text=}

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

[Remove-AzureADTrustedCertificateAuthority](Remove-AzureADTrustedCertificateAuthority.md)

[Set-AzureADTrustedCertificateAuthority](Set-AzureADTrustedCertificateAuthority.md)

