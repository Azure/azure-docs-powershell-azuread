---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: D74563F0-14B9-43BD-8C3C-BC46CD505407
online version: 
schema: 2.0.0
---

# Remove-AzureADPolicy

## SYNOPSIS
Removes a policy.

## SYNTAX

```
Remove-AzureADPolicy -ObjectId <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADPolicy** cmdlet removes a policy from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove a policy
```
PS C:\>Remove-AzureADPolicy -ObjectId *<objectID>*.
```

This command removes the specified policy.

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
Specifies the object ID of the policy to remove.

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

[Get-AzureADPolicy](./Get-AzureADPolicy.md)

[New-AzureADPolicy](./New-AzureADPolicy.md)

[Set-AzureADPolicy](./Set-AzureADPolicy.md)
