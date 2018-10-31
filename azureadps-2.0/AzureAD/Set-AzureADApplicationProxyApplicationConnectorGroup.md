---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationProxyApplicationConnectorGroup

## SYNOPSIS
The Set-AzureADApplicationProxyApplicationConnectorGroup cmdlet assigns the given connector group to a specified application. 

## SYNTAX

```
Set-AzureADApplicationProxyApplicationConnectorGroup -ObjectId <String> -ConnectorGroupId <String>
```

## DESCRIPTION
The Set-AzureADApplicationProxyApplicationConnectorGroup cmdlet sets the connector group assigned for the specified application. The application must be configured for Application Proxy in Azure Active Directory (AD). 

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADApplicationProxyApplicationConnectorGroup -ObjectId 59462d3c-a1bc-40a0-9bed-be799357ebce -ConnectorGroupId a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 
```
Example 1: Set a new Connector Group for a specific application

## PARAMETERS

### -ConnectorGroupId
The Id of the Connector group that should be assigned to the application. You can find this by using the Get-AzureADApplicationProxyConnectorGroup command.

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

### -ObjectId
The unique application Id for the application the Connector group will be assigned to. This can be found using the Get-AzureADApplication command.

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

