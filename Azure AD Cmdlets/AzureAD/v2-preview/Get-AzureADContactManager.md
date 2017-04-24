---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 45AD85CB-E30B-412B-945E-64187DD0E9BA
online version: 
schema: 2.0.0
---

# Get-AzureADContactManager

## SYNOPSIS
Gets the manager of a contact.

## SYNTAX

```
Get-AzureADContactManager -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADContactManager** cmdlet gets the manager of a contact in Azure Active Directory.

## EXAMPLES

### Example 1: Get the manager of a contact
```
PS C:\> $Contact = Get-AzureADContact -Top 1
PS C:\> Get-AzureADContactManager -ObjectId $Contact.ObjectId
```

The first command gets a contact by using the [Get-AzureADContact](./Get-AzureADContact.md) cmdlet, and then stores it in the $Contact variable.

The second command gets the manager for $Contact.

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

### -ObjectId
Specifies the ID of a contact in Azure Active Directory.

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

[Get-AzureADContact](./Get-AzureADContact.md) 

[Remove-AzureADContactManager](./Remove-AzureADContactManager.md)

[Set-AzureADContactManager](./Set-AzureADContactManager.md)
