---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-GovernanceRoleAssignments

## SYNOPSIS
Get role assignments for a specific provider and resource

## SYNTAX

```
Get-GovernanceRoleAssignments [-Filter <String>] -ProviderId <String> -ResourceId <String> [-Top <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Get role assignments for a specific provider and resource

## EXAMPLES

### Example 1
```
PS C:\> Get-GovernanceRoleAssignments -ProviderId AzureResources -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9
```

Get all role assignments for a specific provider and resource

## PARAMETERS

### -Filter
The Odata filter

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -Top
The top count

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

### System.String
### System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
