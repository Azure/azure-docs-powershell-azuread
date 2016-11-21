---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDeviceRegisteredOwner

## SYNOPSIS
Get users that are registered as owner on the device.

## SYNTAX

```
Get-AzureADDeviceRegisteredOwner -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the registered owner of a device
```
$DevId = (get-azureaddevice -top 1).objectid
Get-AzureADDeviceRegisteredOwner -ObjectId $DevId
```

This example retrieves the registered owner of a device

## PARAMETERS

### -ObjectId
The unique identifier of the device

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

