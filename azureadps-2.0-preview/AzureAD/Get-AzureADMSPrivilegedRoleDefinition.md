---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSPrivilegedRoleDefinition

## SYNOPSIS
Get role definitions

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPrivilegedRoleDefinition -ProviderId <String> -ResourceId <String> [-Top <Int32>]
 [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPrivilegedRoleDefinition -ProviderId <String> -ResourceId <String> -Id <String>
 [<CommonParameters>]
```

## DESCRIPTION
Get role definitions

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSPrivilegedRoleDefinition -ProviderId AzureResources -ResourceId a0a0a0a0-bbbb-cccc-dddd-e1e1e1e1e1e1 -Top 10
```

Get role definitions for a specific provider and resource

### Example 1
```
PS C:\> Get-AzureADMSPrivilegedRoleDefinition -ProviderId AzureResources -ResourceId a0a0a0a0-bbbb-cccc-dddd-e1e1e1e1e1e1 -Id b1b1b1b1-cccc-dddd-eeee-f2f2f2f2f2f2
```

Get a role definitions for a specific provider, resource and Id

## PARAMETERS

### -Id
The id of a role definition

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

### -Filter
{{ Fill Filter Description }}

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

### -Top
{{ Fill Top Description }}

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
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
