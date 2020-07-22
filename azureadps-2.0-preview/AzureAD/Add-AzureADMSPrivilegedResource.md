---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMSPrivilegedResource

## SYNOPSIS
Use this API to add a new azure AD MS privileged resource.

## SYNTAX

```
Add-AzureADMSPrivilegedResource -ProviderId <String> [-ExternalId <String>] [<CommonParameters>]
```

## DESCRIPTION
Use this API to add a new azure AD MS privileged resource.

## EXAMPLES

### Example 1
```
PS C:\> Add-AzureADMSPrivilegedResource -ProviderId AzureResources -ExternalId "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d"
```

Register a new Resource

## PARAMETERS

### -ExternalId
The unique identifier of the specific resource Id

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
