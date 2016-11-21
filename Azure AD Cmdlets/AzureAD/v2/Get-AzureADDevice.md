---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDevice

## SYNOPSIS
Retrieves a specific device from Azure Active Directory

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-AzureADDevice [-Top <Nullable`1[Int32]>] [-Filter <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-AzureADDevice [-SearchString <String>]
```

### UNNAMED_PARAMETER_SET_3
```
Get-AzureADDevice -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve a device based on ObjectId
```
$DeviceId = (Get-AzureADDevice -Top 1).ObjectId
Get-AzureADDevice -ObjectId $DeviceId

ObjectId                             DeviceId                             DisplayName
--------                             --------                             -----------
3cb87a8f-0a41-4ca8-8910-e56cc00114a3 48445467-033c-42ca-8e38-8d181db1d49c bastias_WindowsPhone_5/1/2016_12:53 PM
```

### Retrieve all devices from your directory
```
Get-AzureADDevice

Output:

ObjectId                             DeviceId                             DisplayName
--------                             --------                             -----------
3cb87a8f-0a41-4ca8-8910-e56cc00114a3 48445467-033c-42ca-8e38-8d181db1d49c bastias_WindowsPhone_5/1/2016_12:53 PM
62aae804-8b1a-4ab7-8fda-5068aed1a1f7 3cb87a8f-0a41-4ca8-8910-e56cc00114a3 New Device
d4fe7726-5966-431c-b3b8-cddc8fdb717d 293872f6-c006-4e6a-8629-07847c5ab078 New Device
```

### Retrieve a device from the directory, filter on DeviceId
```
Get-AzureADDevice -Filter "deviceId eq guid'85e05cd0-bbc8-4765-bee6-1ebcb667ccef'"
```

## PARAMETERS

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Filter
The filter parameter can be used to filter returned objects of a cmdlet using an Odata filter statement.
An example would be 

Get-AzureADDevice -Filter "DisplayName eq 'TestName'"

which would only return device objects for which the DisplayName equals "TestName".

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
The SearchString parameter allows you to search for specific objects.
This includes the DisplayName and Description attribute as well as addtional string attributes for an object

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The unique identifier of a device in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

