---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 5810982A-C9A8-4A13-BE28-5D9CB053DB1A
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Enable-MsolDevice

## SYNOPSIS
Enables a device object in Azure Active Directory.

## SYNTAX

### EnableDeviceByDeviceId (Default)
```
Enable-MsolDevice -DeviceId <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnableDeviceByObjectId
```
Enable-MsolDevice [-Force] -ObjectId <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-MsolDevice** cmdlet enables a device object in Azure Active Directory.

## EXAMPLES

### Example 1: Enable a device using a device ID with confirmation
```
PS C:\>Enable-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274"
```

This command enables the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Azure Active Directory.
This command prompts the user for confirmation.

### Example 2: Enable a device using a device ID
```
PS C:\>Enable-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274" -Force
```

This command enables the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Azure Active Directory.
Since the command uses the *Force* parameter, the user is not prompted for confirmation.

## PARAMETERS

### -DeviceId
Specifies the device ID of the device that this cmdlet enables.

```yaml
Type: Guid
Parameter Sets: EnableDeviceByDeviceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the device that this cmdlet enables.

```yaml
Type: Guid
Parameter Sets: EnableDeviceByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the command.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

###  
This cmdlet does not generate any output.

## NOTES

## RELATED LINKS

[Disable-MsolDevice](./Disable-MsolDevice.md)

[Get-MsolDevice](./Get-MsolDevice.md)

[Remove-MsolDevice](./Remove-MsolDevice.md)
