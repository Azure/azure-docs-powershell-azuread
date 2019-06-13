---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-GovernanceRoleSetting

## SYNOPSIS
Get role setting

## SYNTAX

```
Get-GovernanceRoleSetting -Id <String> -ProviderId <String> [<CommonParameters>]
```

## DESCRIPTION
Get role setting

## EXAMPLES

### Example 1
```
PS C:\> Get-GovernanceRoleSetting -ProviderId AzureResources -Id 4b95b664-7434-48e6-8dec-34caf4d8c3bd
```

Get role setting for a specific provider id and setting id

## PARAMETERS

### -Id
The unique identifier of the specific role setting

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

### -ProviderId
The unique identifier of the specific provider

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

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
