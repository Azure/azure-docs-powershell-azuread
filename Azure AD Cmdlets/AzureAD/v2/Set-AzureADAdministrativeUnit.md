---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
ms.assetid: 80D775B6-1EA6-4F54-A727-A981B0CBC3A1
online version: 
schema: 2.0.0
---

# Set-AzureADAdministrativeUnit

## SYNOPSIS
Updates an administrative unit.

## SYNTAX

```
Set-AzureADAdministrativeUnit -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-Description <String>] [-DisplayName <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADAdministrativeUnit** cmdlet updates an administrative unit in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -Description
Specifies a description.
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

### -DisplayName
Specifies a display name.

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

### -ObjectId
Specifies the ID of an administrative unit in Azure AD.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADAdministrativeUnit](./Get-AzureADAdministrativeUnit.md)

[New-AzureADAdministrativeUnit](./New-AzureADAdministrativeUnit.md)

[Remove-AzureADAdministrativeUnit](./Remove-AzureADAdministrativeUnit.md)
