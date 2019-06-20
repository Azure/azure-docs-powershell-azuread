---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Close-GovernanceRoleAssignmentRequest

## SYNOPSIS
Cancels a GovernanceRoleAssignmentRequest

## SYNTAX

```
Close-GovernanceRoleAssignmentRequest -Id <String> -ProviderId <String> [<CommonParameters>]
```

## DESCRIPTION
Cancel a GovernanceRoleAssignmentRequest

## EXAMPLES

### Example 1
```
PS C:\> Close-GovernanceRoleAssignmentRequest -ProviderId AzureResources -Id 14eda86f-b650-4ccf-802f-33842c1f1d2c
```

Cancel a request for AzureResources provider

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
