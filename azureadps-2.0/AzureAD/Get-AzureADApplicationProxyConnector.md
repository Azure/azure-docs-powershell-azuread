---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnector

## SYNOPSIS
The Get-AzureADApplicationProxyApplicationConnector cmdlet a list of all connectors, or if specified, details of a specific connector.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADApplicationProxyConnector [-All <Boolean>] [-Top <Int32>] [-Filter <String>]
```

### GetVague
```
Get-AzureADApplicationProxyConnector [-SearchString <String>] [-All <Boolean>]
```

### GetById
```
Get-AzureADApplicationProxyConnector -Id <String> [-All <Boolean>]
```

## DESCRIPTION
The Get-AzureADApplicationProxyApplicationConnector cmdlet retrieves the details for a given connector. If no connectorId is specified, it retrieves all the connectors assigned to the tenant.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyConnector

Id                                   MachineName                      ExternalIp     Status
--                                   -----------                      ----------     ------
4c8b06e7-9751-41d5-8e5e-48e9b9bc2c66 AWCyclesApps.adventure-works.com 52.165.149.115 active
834c5dd6-f2e8-47ae-973a-9fc769289b3d AWCyclesAD.adventure-works.com   52.165.149.131 active 
```
Example 1: Retrieve all connectors


### Example 2
```
PS C:\> Get-AzureADApplicationProxyConnector -Id 4c8b06e7-9751-41d5-8e5e-48e9b9bc2c66

Id                                   MachineName                      ExternalIp     Status
--                                   -----------                      ----------     ------
4c8b06e7-9751-41d5-8e5e-48e9b9bc2c66 AWCyclesApps.adventure-works.com 52.165.149.115 active 
```
Example 2: Retrieve information for a specific connector 

## PARAMETERS

### -All
If true, return all users. If false, return the number of objects specified by the Top parameter

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

### -Filter
Specifies an oData v3.0 filter statement. This parameter controls which objects are returned. Details on querying with oData can be found here: http://www.odata.org/documentation/odata-version-3-0/odata-version-3-0-core-protocol/#queryingcollections

```yaml
Type: String
Parameter Sets: GetQuery
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
The Id of the specific connector. You can find this by running the command without this parameter to get the desired Id, or by going into the portal and viewing connector details.

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.

```yaml
Type: String
Parameter Sets: GetVague
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

