---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnectorMemberOf

## SYNOPSIS
The Get-AzureADApplicationProxyConnectorMemberOf command gets the ConnectorGroup that the specified Connector is a member of.

## SYNTAX

```
Get-AzureADApplicationProxyConnectorMemberOf -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADApplicationProxyConnectorMemberOf command gets the ConnectorGroup that the specified Connector is a member of.
If no group has been assigned to the connector, by default it will be in 'Default'.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyConnectorMemberOf -Id 4c8b06e7-9751-41d5-8e5e-48e9b9bc2c66

Id                                   Name                ConnectorGroupType IsDefault
--                                   ----                ------------------ ---------
a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 Application Servers applicationProxy       False
```

## PARAMETERS

### -Id
The Id of the connector.
You can find this by running Get-AzureADApplicationProxyConnector.

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
