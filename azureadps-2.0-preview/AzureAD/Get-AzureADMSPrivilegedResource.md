---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSPrivilegedResource

## SYNOPSIS
Get azure AD MS privileged resource

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPrivilegedResource -ProviderId <String> [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPrivilegedResource -ProviderId <String> -Id <String> [<CommonParameters>]
```

## DESCRIPTION
Get azure AD MS privileged resource

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSPrivilegedResource -ProviderId AzureResources -Id 3f5887ed-dd6e-4821-8bde-c813ec508cf9
```

Get a resource for AzureResource provider with Id

### Example 2
```
PS C:\> Get-AzureADMSPrivilegedResource -ProviderId AzureResources
```

Get all resources for AzureResource provider

## PARAMETERS

### -Filter
The filter for Odata query

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

### -Id
The unique identifier of the specific resource

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

### -Top
The top result count

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
