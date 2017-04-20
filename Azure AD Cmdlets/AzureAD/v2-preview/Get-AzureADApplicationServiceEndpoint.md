---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationServiceEndpoint

## SYNOPSIS
Retrieve the service endpoint of an application

## SYNTAX

```
Get-AzureADApplicationServiceEndpoint -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet retrieves the service endpoint(s) of an application. The service endpoint entity contains service discovery information. The serviceEndpoints property of the Application entitie is of type ServiceEndpoint. Other services can use the information stored in the ServiceEndpoint entity to find this service and its addressable endpoints. 

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADApplicationServiceEndpoint -ObjectId 79592454-dea7-4660-9d91-f1768e5055ac
```

Retrieves the Service EndPoint of the application that is specified through the Object ID parameter

## PARAMETERS

### -All
Return all service endpoints 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies the object ID of the application for which the service endpoint is retrieved

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

### -Top
specifies the maximum number of results that are returned. the default is 100.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

