---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-GovernanceRoleAssignment

## SYNOPSIS
Get a governance role assignment

## SYNTAX

```
Get-GovernanceRoleAssignment -Id <String> -ProviderId <String> -ResourceId <String> [<CommonParameters>]
```

## DESCRIPTION
Get a governance role assignment

## EXAMPLES

### Example 1
```
PS C:\> Get-GovernanceRoleAssignments -ProviderId AzureResources -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9
```

Get all role assignments for a specific resource

### Example 2
```
PS C:\> Get-GovernanceRoleAssignment -ProviderId AzureResources -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9 -Id b83c177a-10e0-4eeb-8d0b-f3668fbf81fa
```

Get a role assignment for a specific resource with assignment id

## PARAMETERS

### -Id
The unique identifier of the specific role assignment

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

### -ResourceId
The unique identifier of the specific resource

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
