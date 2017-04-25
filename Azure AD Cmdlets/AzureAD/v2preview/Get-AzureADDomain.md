---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 04497A4E-E281-4FB5-98D5-102039F15692
online version: 
schema: 2.0.0
---

# Get-AzureADDomain

## SYNOPSIS
Gets a domain.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDomain [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADDomain -Name <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDomain** cmdlet gets a domain in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

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

### -Name
Specifies the name of a domain.
```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Confirm-AzureADDomain](./Confirm-AzureADDomain.md)
[New-AzureADDomain](./New-AzureADDomain.md)
[Remove-AzureADDomain](./Remove-AzureADDomain.md)
[Set-AzureADDomain](./Set-AzureADDomain.md)


