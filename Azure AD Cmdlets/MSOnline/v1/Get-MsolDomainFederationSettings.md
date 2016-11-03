---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 14330E4B-4E9C-4A11-8A11-47222B149052
---

# Get-MsolDomainFederationSettings

## SYNOPSIS
Retrieves settings for a federated domain.

## SYNTAX

```
Get-MsolDomainFederationSettings -DomainName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolDomainFederationSettings cmdlet gets key settings from Microsoft Azure Active Directory.
Use the Get-MSOLFederationProperty cmdlet to get settings for both Microsoft Azure Active Directory and the Active Directory Federation Services server.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolDomainFederationSettings -DomainName contoso.com

          Returns the federation settings for contoso.com.
```

Description

-----------

Returns the federation settings for contoso.com.

## PARAMETERS

### -DomainName
The fully qualified domain name to retrieve.

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
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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

            ActiveLogOnUri
            FederationBrandName
            IssuerUri
            LogOffUri
            MetadataExchangeUri
            NextSigningCertificate
            PassiveLogOnUri
            SigningCertificate

## NOTES

## RELATED LINKS


