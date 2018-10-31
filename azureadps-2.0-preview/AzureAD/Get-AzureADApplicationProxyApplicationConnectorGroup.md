---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyApplicationConnectorGroup

## SYNOPSIS
The Get-AzureADApplicationProxyApplicationConnectorGroup cmdlet retrieves the connector group assigned for a specific application.

## SYNTAX

```
Get-AzureADApplicationProxyApplicationConnectorGroup -ObjectId <String>
```

## DESCRIPTION
The Get-AzureADApplicationProxyApplicationConnectorGroup cmdlet retrieves the connector group assigned for the specified application. The application must be configured for Application Proxy in Azure Active Directory (AD). 

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyApplicationConnectorGroup -ObjectId 8d6c6684-6f8c-42e2-8914-32ed2adf9ccf

Id                                   Name                ConnectorGroupType IsDefault
--                                   ----                ------------------ ---------
a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 Application Servers applicationProxy       False 
```

## PARAMETERS

### -ObjectId
ObjectId is the Id of the application. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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

