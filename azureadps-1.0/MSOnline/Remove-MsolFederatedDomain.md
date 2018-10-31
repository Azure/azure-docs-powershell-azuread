---
external help file: Microsoft.Online.Identity.Federation.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 59811DE6-DD0A-4F11-B16D-842EB397F5EE
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolFederatedDomain

## SYNOPSIS
Removes a single sign-on domain from the domains in Microsoft Online.

## SYNTAX

```
Remove-MsolFederatedDomain [-SupportMultipleDomain] -DomainName <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolFederatedDomain** cmdlet removes the specified single sign-on domain from Microsoft Online and the associated relying party trust settings in Active Directory Federation Services 2.0.

If the domain specified has objects associated with it, you cannot remove the domain.

## PARAMETERS

### -DomainName
Specifies the name of the single sign-on domain to remove. 

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
[New-MsolFederatedDomain](./New-MsolFederatedDomain.md)

[Update-MsolFederatedDomain](./Update-MsolFederatedDomain.md)
