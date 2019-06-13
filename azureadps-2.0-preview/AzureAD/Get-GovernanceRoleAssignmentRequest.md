---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-GovernanceRoleAssignmentRequest

## SYNOPSIS
Get governance role assignment request

## SYNTAX

```
Get-GovernanceRoleAssignmentRequest -Id <String> -ProviderId <String> [<CommonParameters>]
```

## DESCRIPTION
Get governance role assignment request

## EXAMPLES

### Example 1
```
PS C:\> Get-GovernanceRoleAssignmentRequest -ProviderId AzureResources -Id 14eda86f-b650-4ccf-802f-33842c1f1d2c
```

Get a role assignment request for AzureResources provider with a role assignment id

## PARAMETERS

### -Id
The unique identifier of the specific role assignment request

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
