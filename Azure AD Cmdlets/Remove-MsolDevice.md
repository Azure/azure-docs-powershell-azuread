---
external help file: AzureADHelpMSOL.xml
online version: 58f7425a-3f73-4caf-851d-972214e870ac
schema: 2.0.0
---

# Remove-MsolDevice

## SYNOPSIS
Remove a device object from Azure Active Directory.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Remove-MsolDevice [-Force] -DeviceId <Guid> [-Confirm] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_2
```
Remove-MsolDevice [-Force] -ObjectId <Guid> [-Confirm] [-WhatIf]
```

## DESCRIPTION
The **Remove-MsolDevice** cmdlet removes a device object from Azure Active Directory.

## EXAMPLES

### Example 1: Remove a device by device ID with confirmation
```
PS C:\>Remove-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274"
```

This command removes the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Azure Active Directory.
Since the command does not use the *Force* parameter, the user is prompted for confirmation.

### Example 2: Remove a device by device ID
```
PS C:\>Remove-MsolDevice -DeviceId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274" -Force
```

This command removes the device with DeviceId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Azure Active Directory.
Since the command uses the *Force* parameter, the user is not prompted for confirmation.

### Example 3: Remove a device by object ID
```
PS C:\>Remove-MsolDevice -ObjectId "1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274"
```

This command removes the device with ObjectId 1aa200c4-bdfb-42b5-9a1e-5f1bafbe4274 from Azure Active Directory.

## PARAMETERS

### -DeviceId
Specifies the device ID of the device that this cmdlet removes.

```yaml
Type: Guid
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
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
Specifies the unique object ID of the device that this cmdlet removes.

```yaml
Type: Guid
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Microsoft.Online.Administration.Device, System.Guid
You can pipe **Microsoft.Online.Administration.Device** objects that contain an **ObjectId** or **DeviceId**.
You can also pipe a device, **ObjectId**, or **DeviceId** as a string.

## OUTPUTS

### 
This cmdlet does not generate any output.

## NOTES

## RELATED LINKS

[Disable-MsolDevice](58f7425a-3f73-4caf-851d-972214e870ac)

[Enable-MsolDevice](5810982a-c9a8-4a13-be28-5d9cb053db1a)

[Get-MsolDevice](b11640a7-18c4-475a-b6be-d16957c4f58c)

