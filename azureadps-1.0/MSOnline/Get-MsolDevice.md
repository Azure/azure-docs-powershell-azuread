---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: B11640A7-18C4-475A-B6BE-D16957C4F58C
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolDevice

## SYNOPSIS
Gets an individual device, or a list of devices.

## SYNTAX

### GetDeviceByDeviceName (Default)
```
Get-MsolDevice -Name <String> [<CommonParameters>]
```

### GetDeviceAll
```
Get-MsolDevice [-All] [-ReturnRegisteredOwners] [<CommonParameters>]
```

### GetDeviceByDeviceId
```
Get-MsolDevice -DeviceId <Guid> [<CommonParameters>]
```

### GetDeviceByLogonTimestamp
```
Get-MsolDevice -All -LogonTimeBefore <DateTime> [<CommonParameters>]
```

### GetDeviceByObjectId
```
Get-MsolDevice -ObjectId <Guid> [<CommonParameters>]
```

### GetDeviceByRegisteredOwner
```
Get-MsolDevice -RegisteredOwnerUpn <String> [<CommonParameters>]
```

### GetDeviceIncludeSystemManaged
```
Get-MsolDevice -All -IncludeSystemManagedDevices [<CommonParameters>]
```
## DESCRIPTION
The **Get-MsolDevice** cmdlet gets an individual device, or a list of devices.

## EXAMPLES

### Example 1: Get a device object
```
PS C:\>Get-MsolDevice -Name "NIC0123"
```

This command gets a device object that is named NIC0123.

### Example 2: Get a list of device objects
```
PS C:\>Get-MsolDevice -All
```

This command gets a list of device objects.
Since the *ReturnRegisteredOwners* parameter is not used, the device object does not contain the **registeredOwners** property.

### Example 3: Get a list of device objects that contains the registeredOwners property
```
PS C:\>Get-MsolDevice -All -ReturnRegisteredOwners
```

This command gets a list of device objects.
Since the *ReturnRegisteredOwners* parameter is used, the device object contains the **registeredOwners** property.

### Example 4: Get a device by device ID
```
PS C:\>Get-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274"
```

This command gets a device with the corresponding device ID.

### Example 5: Get a device object by object ID
```
PS C:\>Get-MsolDevice -ObjectId "566F7EA7-7BF1-4F4A-AF23-A1B46DBD46D6"
```

This command gets a device with the corresponding object ID.

### Example 6: Get devices registered by UPN
```
PS C:\>Get-MsolDevice -RegisteredOwnerUpn "pattifuller@contoso.com"
```

This command gets all the devices registered by the user with the UPN named pattifuller@contoso.com.

### Example 7: Get device by activity (logon) timestamp
```
PS C:\>Get-MsolDevice -All -LogonTimeBefore 'January 1, 2017 12:00:00 AM'
```

Ths command gets all the devices with the ApproximateLastLogonTimestamp before January 1, 2017

### Example 8: Get devices and include system managed devices
```
PS C:\>Get-MsolDevice -All -IncludeSystemManagedDevices
```

This command gets all devices and includes auto-pilot devices and other devices that are used with Intune (e.g. EAS)

## PARAMETERS

### -All
Indicates that this cmdlet returns all results.

```yaml
Type: SwitchParameter
Parameter Sets: GetDeviceAll
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
Specifies the device ID of the device that this cmdlet gets.

```yaml
Type: Guid
Parameter Sets: GetDeviceByDeviceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -IncludeSystemManagedDevices
Indicates that this cmdlet includes devices that are managed by the system such as auto-pilot.

```yaml
Type: SwitchParamater
Parameter Sets: GetDeviceIncludeSystemManaged
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -LogonTimeBefore
Specified the date (UTC) used to filter the device list by.

```yaml
Type: DateTime
Parameter Sets: GetDeviceByLogonTimestamp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the display name of the device that this cmdlet gets.

```yaml
Type: String
Parameter Sets: GetDeviceByDeviceName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the device that this cmdlet gets.

```yaml
Type: Guid
Parameter Sets: GetDeviceByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegisteredOwnerUpn
Specifies the user object that is the registered owner of the device.
You need to provide the user principal name (UPN) or *ObjectId*, or pass an instance of a **Microsoft.Online.Administration.User** object that contains the user's UPN or ObjectId.

```yaml
Type: String
Parameter Sets: GetDeviceByRegisteredOwner
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReturnRegisteredOwners
Indicates that this cmdlet returns the device's **registeredOwners** property.

```yaml
Type: SwitchParameter
Parameter Sets: GetDeviceAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Device
This cmdlet returns device objects, which include the following information: 

- AccountEnabled: The device's status: enabled or disabled. 
- ObjectId: The device's unique ID. 
- DeviceId: The device's device ID. 
- DisplayName: The device's display name. 
- DeviceObjectVersion: The device's object version number. 
- DeviceOSType: The device operating system type. 
- DeviceOSVersion: The device operating system version number. 
- DeviceTrustType: The device trust type.
The value could be one of the following: Workplace Joined, AzureAD Joined, Domain Joined. 
- DeviceTrustLevel: The device trust level.
The value could be one of the following: Authenticated, Compliant, Managed. 
- DevicePhysicalIds: The device physical Ids. 
- ApproximateLastLogonTimestamp: The last logon timestamp using this device. 
- AlternativeSecurityIds: The device alternative security Ids. 
- DirSyncEnabled: If the device is enabled with DirSync. 
- LastDirSyncTime: The last timestamp the device was synchronized by DirSync. 
- RegisteredOwners: The device's registered owner. 
- GraphDeviceObject: The device object returned from graph API.

## NOTES

## RELATED LINKS

[Disable-MsolDevice](./Disable-MsolDevice.md)

[Enable-MsolDevice](./Enable-MsolDevice.md)

[Remove-MsolDevice](./Remove-MsolDevice.md)


