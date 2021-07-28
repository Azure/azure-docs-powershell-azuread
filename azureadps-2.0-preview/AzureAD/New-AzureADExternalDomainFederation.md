---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADExternalDomainFederation

## SYNOPSIS
Create a new externalDomainFederation in Azure Active Directory

## SYNTAX

```
New-AzureADExternalDomainFederation [-ExternalDomainName <String>]
 [-FederationSettings <DomainFederationSettings>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Create a new external domain federation.
```
$federationSettings = New-Object Microsoft.Open.AzureAD.Model.DomainFederationSettings
$federationSettings.ActiveLogOnUri="https://adfs.com/adfs/ls"
$federationSettings.IssuerUri = "http://adfs.com/adfs/services/trust"
$federationSettings.LogOffUri = $federationSettings.ActiveLogOnUri
$federationSettings.FederationBrandName = "Contoso Misa1 US"
$federationSettings.MetadataExchangeUri="http://adfs.com/FederationMetadata.xml"
$federationSettings.PassiveLogOnUri=$federationSettings.ActiveLogOnUri
$federationSettings.PreferredAuthenticationProtocol="WsFed"
$federationSettings.SigningCertificate="X509 signing public key"
New-AzureADExternalFederationDomain -ExternalDomainName "adfs.com" -FederationSettings $federationSettings
```

This command creates a new external federation domain settings.

## PARAMETERS

### -ExternalDomainName
The unique identifer of an externalDomainFederation in Azure Active Directory

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FederationSettings
The federation settings for the external domain.

```yaml
Type: DomainFederationSettings
Parameter Sets: (All)
Aliases:

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
