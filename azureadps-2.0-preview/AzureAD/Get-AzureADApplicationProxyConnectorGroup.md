---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnectorGroup

## SYNOPSIS
The Get-AzureADApplicationProxyConnectorGroup cmdlet retrieves a list of all connector groups, or if specified, details of a specific connector group. 

## SYNTAX

### GetQuery (Default)
```
Get-AzureADApplicationProxyConnectorGroup [-All <Boolean>] [-Top <Int32>] [-Filter <String>]
```

### GetVague
```
Get-AzureADApplicationProxyConnectorGroup [-SearchString <String>] [-All <Boolean>]
```

### GetById
```
Get-AzureADApplicationProxyConnectorGroup -Id <String> [-All <Boolean>]
```

## DESCRIPTION
The Get-AzureADApplicationProxyConnectorGroup cmdlet retrieves a list of all connector groups, or if specified, details of the specified connector group.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyConnectorGroup

Id                                   Name                ConnectorGroupType IsDefault
--                                   ----                ------------------ ---------
1a0bc41a-8663-4da3-934c-214640663a33 Default             applicationProxy        True
68348ab6-4cc5-4c8c-a0f0-7a43db2f4ff6 Guest Applications  applicationProxy       False
a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 Application Servers applicationProxy       False
``` 
Example 1: Retrieve all connector groups

### Example 2
```
PS C:\Users\nanaeh\Desktop\Microsoft.Open.AzureAD.Module.Preview> Get-AzureADApplicationProxyConnectorGroup -Id a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84

Id                                   Name                ConnectorGroupType IsDefault
--                                   ----                ------------------ ---------
a39b9095-8dc8-4d3a-86c3-e7b5c3f0fb84 Application Servers applicationProxy       False 
```
Example 2: Retrieve a specific connector groups

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
The Id of the specific connector group. You can find this by running the command without this parameter to get the desired Id, or by going into the portal and viewing connector group details.

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
Specifies the search string.

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

