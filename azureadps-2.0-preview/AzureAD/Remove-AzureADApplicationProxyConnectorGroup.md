---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationProxyConnectorGroup

## SYNOPSIS
The Remove-AzureADApplicationProxyApplicationConnectorGroup cmdlet deletes an Application Proxy Connector group. 

## SYNTAX

```
Remove-AzureADApplicationProxyConnectorGroup -Id <String>
```

## DESCRIPTION
The Remove-AzureADApplicationProxyConnectorGroup cmdlet deletes an Application Proxy Connector Group. It can only be used on an empty connector group, with no connectors assigned. 

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADApplicationProxyApplicationConnectorGroup -ObjectId 59462d3c-a1bc-40a0-9bed-be799357ebce 
```
Example 1: Remove a specific Connector Group

## PARAMETERS

### -Id
The Id of the Connector group to delete. You can find this value by running the Get-AzureADApplicationProxyConnectorGroup command. 

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

