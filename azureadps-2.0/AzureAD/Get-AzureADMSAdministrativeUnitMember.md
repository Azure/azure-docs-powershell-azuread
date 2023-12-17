---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSAdministrativeUnitMember

## SYNOPSIS
Gets a member of an administrative unit.

## SYNTAX

```
Get-AzureADMSAdministrativeUnitMember -Id <String> [-All <Boolean>] [-Top <Int32>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSAdministrativeUnitMember cmdlet gets a member of a Microsoft Entra ID administrative unit.

## EXAMPLES

### Example 1 Get an administrative unit member by ID
```
PS C:\> Get-AzureADMSAdministrativeUnitMember -Id "ef08b536-9d0a-4f8f-bda5-8b9cd01a9159"
```

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are: * Continue

* Ignore
* Inquire
* SilentlyContinue
* Stop
* Suspend

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
Specifies a variable in which to store an information event message.

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
Specifies the ID of an administrative unit in the Microsoft Entra ID.

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

### -All
If true, return all administrative unit members.
If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

See the [migration guide for Get-AzureADMSAdministrativeUnitMember](./migrate/Get-AzureADMSAdministrativeUnitMember.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS

[Add-AzureADMSAdministrativeUnitMember](Add-AzureADMSAdministrativeUnitMember.md)

[Remove-AzureADMSAdministrativeUnitMember](Remove-AzureADMSAdministrativeUnitMember.md)

