---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 14330E4B-4E9C-4A11-8A11-47222B149052
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolDomainFederationSettings

## SYNOPSIS
Gets key settings for a federated domain.

## SYNTAX

```
Get-MsolDomainFederationSettings -DomainName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolDomainFederationSettings** cmdlet gets key settings for a federated domain from Azure Active Directory.
Use the [Get-MsolFederationProperty](./Get-MsolFederationProperty.md) cmdlet to get settings for both Azure Active Directory and the Active Directory Federation Services server.

## EXAMPLES

### Example 1: Return federation settings
```
PS C:\> Get-MsolDomainFederationSettings -DomainName "contoso.com"
```

This command returns the federation settings for contoso.com.

## PARAMETERS

### -DomainName
Specifies the fully qualified domain name to retrieve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.DomainFederationSettings
This cmdlet returns the following settings:

* ActiveLogOnUri
* FederationBrandName
* IssuerUri
* LogOffUri
* MetadataExchangeUri
* NextSigningCertificate
* PassiveLogOnUri
* SigningCertificate

## NOTES

## RELATED LINKS
[Get-MsolFederationProperty](./Get-MsolFederationProperty.md)

[Set-MsolDomainFederationSettings](./Set-MsolDomainFederationSettings.md)
