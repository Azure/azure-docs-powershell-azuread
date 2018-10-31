---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 58F7425A-3F73-4CAF-851D-972214E870AC
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Disable-MsolDevice

## SYNOPSIS
Disables a device object in Azure Active Directory.

## SYNTAX

### DisableDeviceByDeviceId (Default)
```
Disable-MsolDevice -DeviceId <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableDeviceByObjectId
```
Disable-MsolDevice [-Force] -ObjectId <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-MsolDevice** cmdlet disables a device object in Azure Active Directory.

## EXAMPLES

### Example 1: Disable a device with confirmation
```
PS C:\>Disable-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274"
```

This command disables the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Microsoft Azure Active Directory.
The command will prompt the user for confirmation.

### Example 2: Disable a device
```
PS C:\>Disable-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274" -Force
```

This command disables the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Microsoft Azure Active Directory.
Since the command uses the *Force* parameter, the user is not prompted for confirmation.

## PARAMETERS

### -DeviceId
Specifies the unique device ID of the device that this cmdlet disables.

```yaml
Type: Guid
Parameter Sets: DisableDeviceByDeviceId
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
Specifies the unique object ID of the device that this cmdlet disables.

```yaml
Type: Guid
Parameter Sets: DisableDeviceByObjectId
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

## NOTES

## RELATED LINKS

[Enable-MsolDevice](./Enable-MsolDevice.md)

[Get-MsolDevice](./Get-MsolDevice.md)

[Remove-MsolDevice](./Remove-MsolDevice.md)
