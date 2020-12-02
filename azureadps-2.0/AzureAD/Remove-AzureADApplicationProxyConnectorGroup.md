---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADApplicationProxyConnectorGroup

## SYNOPSIS
The Remove-AzureADApplicationProxyApplicationConnectorGroup cmdlet deletes an Application Proxy Connector group.

## SYNTAX

```
Remove-AzureADApplicationProxyConnectorGroup -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADApplicationProxyConnectorGroup cmdlet deletes an Application Proxy Connector Group.
It can only be used on an empty connector group, with no connectors assigned.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADApplicationProxyApplicationConnectorGroup -ObjectId 59462d3c-a1bc-40a0-9bed-be799357ebce
```

Example 1: Remove a specific Connector Group

## PARAMETERS

### -Id
The Id of the Connector group to delete.
You can find this value by running the Get-AzureADApplicationProxyConnectorGroup command.

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
