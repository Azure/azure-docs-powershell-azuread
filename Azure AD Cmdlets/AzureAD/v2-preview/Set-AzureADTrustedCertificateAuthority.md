---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: E3628C6F-0F08-49DF-8A48-35E8FF4ABB65
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
The **Set-AzureADTrustedCertificateAuthority** cmdlet updates a trusted certificate authority in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -CertificateAuthorityInformation
Specifies a **CertificateAuthorityInformation** object.

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

[Remove-AzureADTrustedCertificateAuthority](./Remove-AzureADTrustedCertificateAuthority.md)
