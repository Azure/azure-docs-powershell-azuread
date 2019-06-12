---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Add-AzureADServicePrincipalPolicy

## SYNOPSIS
Adds a service principal policy.

## SYNTAX

```
Add-AzureADServicePrincipalPolicy [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 -RefObjectId <String> -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADServicePrincipalPolicy cmdlet adds a service principal policy.

## EXAMPLES

### Example 1: Add a service principal policy
```
PS C:\>Add-AzureADServicePrincipalPolicy -Id <object id of service principal> -RefObjectId <object id of policy>
```

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

### -RefObjectId
Specifies the object Id of the policy.

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

### -Id
The ID of the Service Principal for which you need to set the policy

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

## RELATED LINKS

[Get-AzureADServicePrincipalPolicy]()

[Remove-AzureADServicePrincipalPolicy]()

