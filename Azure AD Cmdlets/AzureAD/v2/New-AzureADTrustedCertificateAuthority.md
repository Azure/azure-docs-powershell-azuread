---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# New-AzureADTrustedCertificateAuthority

## SYNOPSIS

## SYNTAX

```
New-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation <CertificateAuthorityInformation>
```

## DESCRIPTION

## EXAMPLES

### Create a new Trusted Certificate Authority
```
$cert=Get-Content -Encoding byte â€œ[LOCATION OF THE CER FILE FOR THE CERTIFICATE AUTHORITY]â€
$new_ca=New-Object -TypeName Microsoft.Open.AzureAD.Model.CertificateAuthorityInformation
$new_ca.AuthorityType=0
$new_ca.TrustedCertificate=$cert
$new_ca. crlDistributionPoint = â€œ[URL FOR THE CERTIFICATE REVOCATION LIST]â€
New-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation $new_ca
```

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
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[More information about the steps to create a trusted certificate authority can be found here:](https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/)

