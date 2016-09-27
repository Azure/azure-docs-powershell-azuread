---
external help file: AzureADHelpMSOL.xml
online version: 5810982a-c9a8-4a13-be28-5d9cb053db1a
schema: 2.0.0
---

# Disable-MsolDevice

## SYNOPSIS
Disables a device object in Azure Active Directory.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Disable-MsolDevice [-Force] -DeviceId <Guid> [-Confirm] [-WhatIf]
```

### UNNAMED_PARAMETER_SET_2
```
Disable-MsolDevice [-Force] -ObjectId <Guid> [-Confirm] [-WhatIf]
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
Specifies the unique object ID of the device that this cmdlet disables.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-MsolDevice](5810982a-c9a8-4a13-be28-5d9cb053db1a)

[Get-MsolDevice](b11640a7-18c4-475a-b6be-d16957c4f58c)

[Remove-MsolDevice](73c147be-82ec-484f-b2f3-ec684aa7b52c)

