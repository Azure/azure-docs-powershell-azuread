---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 53B15037-19DD-4253-B998-D968DA05F2AC
online version: 
schema: 2.0.0
---

# Set-AzureADDomain

## SYNOPSIS
Updates a domain.

## SYNTAX

```
Set-AzureADDomain -Name <String> [-IsDefault <Boolean>]
 [-SupportedServices <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADDomain** cmdlet updates a domain in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

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
Specifies a name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SupportedServices
Specifies an array of supported services.

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

[New-AzureADDomain](./New-AzureADDomain.md)

[Remove-AzureADDomain](./Remove-AzureADDomain.md)
