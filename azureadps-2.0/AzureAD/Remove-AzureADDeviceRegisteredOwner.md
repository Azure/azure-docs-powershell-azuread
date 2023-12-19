---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADDeviceRegisteredOwner

## SYNOPSIS
Removes the registered owner of a device.

## SYNTAX

```
Remove-AzureADDeviceRegisteredOwner -ObjectId <String> -OwnerId <String> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADDeviceRegisteredOwner cmdlet removes the registered owner of a device in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove an owner from a device
```
PS C:\> $Device = Get-AzureADDevice -Top 1
PS C:\> $Owner = Get-AzureADDeviceRegisteredOwner -ObjectId $Device.ObjectId
PS C:\> Remove-AzureADDeviceRegisteredOwner -ObjectId $Device.ObjectId -OwnerId $Owner.ObjectId
```

The first command gets a device by using the Get-AzureADDevice (./Get-AzureADDevice.md)cmdlet, and then stores it in the $Device variable.

The second command gets the registered owner for the device in $Device by using the Get-AzureADDeviceRegisteredOwner (./Get-AzureADDeviceRegisteredOwner.md)cmdlet.
The command stores it in the $Owner variable.

The final command removes the owner in $Owner from the device in $Device.

## PARAMETERS

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

### -OwnerId
Specifies an owner ID.

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

## NOTES

See the [migration guide for Remove-AzureADDeviceRegisteredOwner](./migrate/Remove-AzureADDeviceRegisteredOwner.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS

[Add-AzureADDeviceRegisteredOwner](Get-AzureADDeviceRegisteredOwner.md)

[Get-AzureADDevice](Get-AzureADDevice.md)

[Get-AzureADDeviceRegisteredOwner](Get-AzureADDeviceRegisteredOwner.md)

