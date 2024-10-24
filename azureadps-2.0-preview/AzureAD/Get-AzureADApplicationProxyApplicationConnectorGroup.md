---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADApplicationProxyApplicationConnectorGroup

## SYNOPSIS
The Get-AzureADApplicationProxyApplicationConnectorGroup cmdlet retrieves the connector group assigned for a specific application.

## SYNTAX

```
Get-AzureADApplicationProxyApplicationConnectorGroup -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADApplicationProxyApplicationConnectorGroup cmdlet retrieves the connector group assigned for the specified application. The application must be configured for Application Proxy in Azure Active Directory (AD). 

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyApplicationConnectorGroup -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
