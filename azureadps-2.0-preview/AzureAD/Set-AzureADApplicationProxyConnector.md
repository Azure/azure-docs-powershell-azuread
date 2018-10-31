---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationProxyConnector

## SYNOPSIS
The Set-AzureADApplicationProxyConnector cmdlet allows reassignment of the connector to another connector group. 

## SYNTAX

```
Set-AzureADApplicationProxyConnector -Id <String> -ConnectorGroupId <String>
```

## DESCRIPTION
The Set-AzureADApplicationProxyConnector cmdlet allows reassignment of the connector to another connector group. 

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADApplicationProxyConnector -Id 834c5dd6-f2e8-47ae-973a-9fc769289b3d -ConnectorGroupId a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 
```
Example 1: Move a Connector to a different Connector Group

## PARAMETERS

### -Id
The Id of the Connector being moved. You can find this value using the Get-AzureADApplicationProxyConnector command.

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

### -ConnectorGroupId
The unique idenfier of the target application proxy connector group in Azure Active Directory. You can find this value using the Get-AzureAdApplicationProxyConnectorGroup command. 

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

## OUTPUTS

## NOTES
## RELATED LINKS

