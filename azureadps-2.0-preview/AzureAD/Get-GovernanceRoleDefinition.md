---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Get-GovernanceRoleDefinition

## SYNOPSIS
Get role definition by id

## SYNTAX

```
Get-GovernanceRoleDefinition [-Filter <String>] -Id <String> -ProviderId <String> -ResourceId <String>
 [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
Get role definition by id

## EXAMPLES

### Example 1
```
PS C:\> Get-GovernanceRoleDefinition -ProviderId AzureResources -ResourceId e5e7d29d-5465-45ac-885f-4716a5ee74b5 -Id ff67e02b-d77b-4588-9f32-e02b7da6539b -Top 10
```

Get role definition for a specific provider, resource and id

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

### -Id
The id of a role definition

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
