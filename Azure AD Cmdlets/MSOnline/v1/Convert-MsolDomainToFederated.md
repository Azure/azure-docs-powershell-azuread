---
external help file: Microsoft.Online.Identity.Federation.PowerShell.dll-help.xml
online version: 
schema: 2.0.0
ms.assetid: 165F509D-D91E-4BE5-AF22-72112C1C3AB7
---

# Convert-MsolDomainToFederated

## SYNOPSIS
Converts the domain from using standard authentication to using single sign-on (also known as identity federation).

## SYNTAX

```
Convert-MsolDomainToFederated [-SupportMultipleDomain] -DomainName <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The Convert-MSOLDomainToFederated cmdlet converts the specified domain from standard authentication to single sign-on (also known as identity federation), including configuring the relying party trust settings between the Active Directory Federation Services 2.0 server and Microsoft Online.
As part of converting a domain from standard authentication to single sign-on, each user must also be converted.
This conversion happens automatically the next time a user signs in; no action is required by the administrator.

## PARAMETERS

### -DomainName
The name of the domain to convert to single sign-on (also known as identity federation).

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

### -Confirm
Prompts you for confirmation before executing the command.

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
Describes what would happen if you executed the command without actually executing the command.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


