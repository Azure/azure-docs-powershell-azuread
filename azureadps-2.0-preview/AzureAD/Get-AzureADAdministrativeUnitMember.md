---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADAdministrativeUnitMember

## SYNOPSIS
Gets a member of an administrative unit.

## SYNTAX

```
Get-AzureADAdministrativeUnitMember -ObjectId <String> [-All <Boolean>] [-Top <Int32>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADAdministrativeUnitMember cmdlet gets a member of an Active Directory administrative unit.

## EXAMPLES

### Example 1 Get an administrative unit member by ID
```
PS C:\> Get-AzureADAdministrativeUnitMember -ObjectId "ef08b536-9d0a-4f8f-bda5-8b9cd01a9159"
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

### -ObjectId
Specifies the ID of an administrative unit in Azure Active Directory.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADAdministrativeUnitMember]()

[Remove-AzureADAdministrativeUnitMember]()

