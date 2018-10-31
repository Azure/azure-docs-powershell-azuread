---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnectorMemberOf

## SYNOPSIS
The Get-AzureADApplicationProxyConnectorMemberOf command gets the ConnectorGroup that the specified Connector is a member of. 

## SYNTAX

```
Get-AzureADApplicationProxyConnectorMemberOf -Id <String>
```

## DESCRIPTION
The Get-AzureADApplicationProxyConnectorMemberOf command gets the ConnectorGroup that the specified Connector is a member of. If no group has been assigned to the connector, by default it will be in 'Default'.

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
The Id of the connector. You can find this by running Get-AzureADApplicationProxyConnector. 

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

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

