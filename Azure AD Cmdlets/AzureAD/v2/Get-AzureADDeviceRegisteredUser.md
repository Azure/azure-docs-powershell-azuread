---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 944E709A-0F66-485C-86E4-1CB4C998C71D
online version: 
schema: 2.0.0
---

# Get-AzureADDeviceRegisteredUser

## SYNOPSIS
Gets a registered user.

## SYNTAX

```
Get-AzureADDeviceRegisteredUser -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDeviceRegisteredUser** cmdlet gets a registered user for an Azure Active Directory device.

## EXAMPLES

### Example 1: Retrieve the registered users of a device
```
PS C:\> $DevId = (Get-AzureADDevice -Top 1).ObjectId
PS C:\> Get-AzureADDeviceRegisteredUser -ObjectId $DevId
```

The first command gets the object ID of a device by using the [Get-AzureADDevice](./Get-AzureADDevice.md) cmdlet, and then stores it in the $DevId variable.  

The second command gets the registered users of the device in $DevId.

## PARAMETERS

### -All
If true, return all registered users. If false, return the number of objects specified by the Top parameter

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
Specifies an object ID.
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

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADDeviceRegisteredUser](./Add-AzureADDeviceRegisteredUser.md)

[Remove-AzureADDeviceRegisteredUser](./Remove-AzureADDeviceRegisteredUser.md)
