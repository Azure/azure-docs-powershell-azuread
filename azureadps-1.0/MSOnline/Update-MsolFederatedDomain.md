---
external help file: Microsoft.Online.Identity.Federation.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 3433FAB9-DA26-483D-BE3C-406FD0C0F746
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Update-MsolFederatedDomain

## SYNOPSIS
Updates the settings in both the Active Directory Federation Services 2.0 server and Microsoft Online.

## SYNTAX

```
Update-MsolFederatedDomain [-SupportMultipleDomain] -DomainName <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Update-MsolFederatedDomain** cmdlet changes settings in both the Active Directory Federation Services 2.0 server and Microsoft Online.
A single sign-on domain is also known as identity-federated domain.

It is necessary to run this cmdlet whenever the URLs or certificate information within Active Directory Federation Services 2.0 change due to configuration changes or through regular maintenance of the certificates, such as when a certificate is about to expire.
This cmdlet should also be run when changes occur in Microsoft Online.
To confirm that the information in the two systems is correct, the [Get-MSOLFederationProperty](./Get-MSOLFederationProperty.md) cmdlet can be used to retrieve the settings.

## PARAMETERS

### -DomainName
Specifies the name of the single sign-on domain to update.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the command.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportMultipleDomain


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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
[Get-MSOLFederationProperty](./Get-MSOLFederationProperty.md)

[New-MsolFederatedDomain](./New-MsolFederatedDomain.md)

[Remove-MsolFederatedDomain](./Remove-MsolFederatedDomain.md)
