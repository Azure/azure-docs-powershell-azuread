---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyConnectorGroupMembers

## SYNOPSIS
The Get-AzureADApplicationProxyConnectorGroupMembers gets all the Application Proxy connectors associated with the given connector group. 

## SYNTAX

```
Get-AzureADApplicationProxyConnectorGroupMembers -Id <String> [-All <Boolean>] [-Top <Int32>]
 [-Filter <String>]
```

## DESCRIPTION
The Get-AzureADApplicationProxyConnectorGroupMembers gets all the Application Proxy connectors associated with the given connector group. 

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyConnectorGroupMembers -Id ba07e273-6b9e-4567-afe4-efddac32509d

Id                                   MachineName     ExternalIp   Status
--                                   -----------     ----------   ------
969eddd2-ad11-47ca-92ba-4442b9901edf vm-test-010 13.93.84.164 active
ea4a4b91-aace-4e8b-b81a-b2f6429a477e test-vm-conn1 52.18.9.115 active
```

The output of this command, showing all the connectors in the group.

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
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
The Id of the Connector group. This can be found by running the Get-AzureADApplicationProxyConnectorGroup command. 

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
Specifies the maximum number of records to return.

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

## INPUTS

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

