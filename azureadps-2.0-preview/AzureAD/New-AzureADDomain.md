---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 29A39191-9E64-4983-8C89-B9A6C574E621
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version: 
schema: 2.0.0
---

# New-AzureADDomain

## SYNOPSIS
Creates a domain.

## SYNTAX

```
New-AzureADDomain [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-IsDefault <Boolean>] -Name <String> [-SupportedServices <System.Collections.Generic.List`1[System.String]>]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADDomain** cmdlet creates a domain in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

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

### -IsDefault
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the domain.

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

### -SupportedServices
```yaml
Type: System.Collections.Generic.List`1[System.String]
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

[Confirm-AzureADDomain](./Confirm-AzureADDomain.md)

[Get-AzureADDomain](./Get-AzureADDomain.md)

[Remove-AzureADDomain](./Remove-AzureADDomain.md)

[Set-AzureADDomain](./Set-AzureADDomain.md)


