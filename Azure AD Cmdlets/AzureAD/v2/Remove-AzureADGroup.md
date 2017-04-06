---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: D495C18D-D65F-4D9E-8A04-C478D1C0F97C
online version: 
schema: 2.0.0
---

# Remove-AzureADGroup

## SYNOPSIS
Removes a group.

## SYNTAX

```
Remove-AzureADGroup -ObjectId <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADGroup** cmdlet removes a group from Azure Active Directory (AD). Note that a Unified Group can be restored withing 30 days after deletion using the Restore-AzureADMSDeletedDirectoryObject cmdlet. Security groups cannot be restored after deletion.

## EXAMPLES

### Example 1: Remove a group
```
PS C:\>Remove-AzureADGroup -ObjectId "11fa5e1e-737c-40c5-835e-416ae3959606"
```

This command removes the specified group from Azure AD.

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

### -ObjectId
Specifies the object ID of a group in Azure AD.

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

[Get-AzureADGroup](./Get-AzureADGroup.md)

[New-AzureADGroup](./New-AzureADGroup.md)

[Set-AzureADGroup](./Set-AzureADGroup.md)
