---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: E5E17FE9-67C1-463F-BC06-B3B6883D99AE
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADDevice

## SYNOPSIS
Gets a device from Active Directory.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDevice [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADDevice [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADDevice -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDevice** cmdlet gets a device from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a device by ID
```
PS C:\>Get-AzureADDevice -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"

ObjectId                             DeviceId                             DisplayName
--------                             --------                             -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 48445467-033c-42ca-8e38-8d181db1d49c bastias_WindowsPhone_5/1/2016_12:53 PM
```

This command gets the specified device.

### Example 2: Get all devices
```
PS C:\>Get-AzureADDevice

ObjectId                             DeviceId                             DisplayName
--------                             --------                             -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 48445467-033c-42ca-8e38-8d181db1d49c bastias_WindowsPhone_5/1/2016_12:53 PM
bbbbbbbb-1111-2222-3333-cccccccccccc aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb New Device
cccccccc-2222-3333-4444-dddddddddddd 293872f6-c006-4e6a-8629-07847c5ab078 New Device
```

This command gets all available devices.

## PARAMETERS

### -All
If true, return all devices. If false, return the number of objects specified by the Top parameter

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
Specifies the oData v3.0 filter statement. This parameter controls which objects are returned.

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

### -ObjectId
Specifies the ID of a device in Azure AD.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADDevice](./New-AzureADDevice.md)
[Remove-AzureADDevice](./Remove-AzureADDevice.md)
[Set-AzureADDevice](./Set-AzureADDevice.md)
