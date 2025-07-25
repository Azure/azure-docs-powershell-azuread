---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSAdministrativeUnit

## SYNOPSIS
Updates an administrative unit.

## SYNTAX

```
Set-AzureADMSAdministrativeUnit -Id <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-Description <String>] [-DisplayName <String>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSAdministrativeUnit cmdlet updates an administrative unit in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -Id
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

See the [migration guide for Set-AzureADMSAdministrativeUnit](./migrate/Set-AzureADMSAdministrativeUnit.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Get-AzureADMSAdministrativeUnit](Get-AzureADMSAdministrativeUnit.md)

[New-AzureADMSAdministrativeUnit](New-AzureADMSAdministrativeUnit.md)

[Remove-AzureADMSAdministrativeUnit](Remove-AzureADMSAdministrativeUnit.md)

