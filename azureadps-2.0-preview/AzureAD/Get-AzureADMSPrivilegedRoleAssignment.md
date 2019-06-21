---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSPrivilegedRoleAssignment

## SYNOPSIS
Get role assignments for a specific provider and resource

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPrivilegedRoleAssignment -ProviderId <String> -ResourceId <String> [-Top <Int32>]
 [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPrivilegedRoleAssignment -ProviderId <String> -ResourceId <String> -Id <String>
 [<CommonParameters>]
```

## DESCRIPTION
Get role assignments for a specific provider and resource

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSPrivilegedRoleAssignment -ProviderId AzureResources -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9
```

Get all role assignments for a specific provider and resource

### Example 2
```
PS C:\> Get-AzureADMSPrivilegedRoleAssignment -ProviderId AzureResources -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9 -Id b83c177a-10e0-4eeb-8d0b-f3668fbf81fa
```

Get a role assignment for a specific provider and resource

## PARAMETERS

### -Filter
The Odata filter

```yaml
Type: String
Parameter Sets: GetQuery
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

### -Id
The unique identifier of the specific role assignment

```yaml
Type: String
Parameter Sets: GetById
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
Parameter Sets: GetQuery
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
