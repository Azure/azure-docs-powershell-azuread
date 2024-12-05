---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADApplicationProxyApplicationConnectorGroup

## SYNOPSIS
The Remove-AzureADApplicationProxyApplicationConnectorGroup cmdlet sets the connector group assigned for the specified application to 'Default' and removes the current assignment. 

## SYNTAX

```
Remove-AzureADApplicationProxyApplicationConnectorGroup -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
If your application is already in the 'Default' group, you will see an error because the application cannot be removed from the 'Default' group unless it is being added to another group. The application must be configured for Application Proxy in Azure Active Directory (AD). 

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADApplicationProxyApplicationConnectorGroup -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb
```

Example 1: Remove the Connector Group associated with an application, setting the group to 'Default'

## PARAMETERS

### -ObjectId
The unique application Id of the application. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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
