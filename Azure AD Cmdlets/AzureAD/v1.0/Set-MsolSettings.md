---
external help file: AzureADHelpMSOL.xml
online version: 22a5d63b-5386-4137-965f-e5cf5696dde5
schema: 2.0.0
---

# Set-MsolSettings

## SYNOPSIS
Updates a directory setting in Azure Active Directory.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-MsolSettings -SettingId <String> -SettingsValue <SettingsValue>
```

### UNNAMED_PARAMETER_SET_2
```
Set-MsolSettings [-SettingId <String>] [-SettingsValue <SettingsValue>] [-TargetObjectId <String>]
 [-TargetType]
```

## DESCRIPTION
The **Set-MsolSettings** cmdlet updates a directory setting in Azure Active Directory.

## EXAMPLES

### Example 1: Update values for a directory setting
```
PS C:\>$OrginSetting = (Get-MsolAllSettings)[0] 
PS C:\> $Value = $OrginSetting.GetSettingsValue() 
PS C:\> $Value["UsageGuidelinesUrl"] = "https://www.contoso.com" 
PS C:\> Set-MsolSettings -SettingId $OriginSetting.Id -SettingsValue $Value
```

This example updates values on the specified directory setting.
The first command uses the **Get-MsolAllSettings** cmdlet to get all directory settings and then stores the results in the variable named $OrginSetting.
The second command then gets the setting values from the $OrginSetting variable and then stores the result in the variable named $Value.
The third command then updates the UsageGuidelinesUrl setting to https://www.contoso.com.
The fourth command then uses the **Set-MsolSettings** cmdlet to update the directory setting.

### Example 2: Update values for a directory setting of a specific group ID
```
PS C:\>$OrginSetting = (Get-MsolAllSettings -TargetType Groups -TargetObjectId "Group011")[0]
PS C:\> $Value = $OrginSetting.GetSettingsValue() 
PS C:\> $Value["UsageGuidelinesUrl"] = "https://www.contoso.com" 
PS C:\> Set-MsolSettings -SettingId $OriginSetting.Id -SettingsValue $Value -TargetType Groups -TargetObjectId "Group011"
```

This example updates values on the specified directory setting.
The first command uses the **Get-MsolAllSettings** cmdlet to get all directory settings for a specific group ID and then stores the results in the variable named $OrginSetting.
The second command then gets the setting values from the $OrginSetting variable and then stores the result in the variable named $Value.
The third command then updates the UsageGuidelinesUrl setting to https://www.contoso.com.
The fourth command then uses the **Set-MsolSettings** cmdlet to update the directory setting.

## PARAMETERS

### -SettingId
Specifies the setting ID associated with the directory setting that this cmdlet gets.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

### -SettingsValue
Specifies the directory setting value that this cmdlet updates the existing setting with.
This operation overwrites the existing setting.

```yaml
Type: SettingsValue
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SettingsValue
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

### -TargetObjectId
Specifies the object ID that settings objects are associated with.
If you do not specify a value, this cmdlet associates the directory setting with the tenant.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

### -TargetType
Specifies the object type that settings objects are associated with.
If you do not specify a value, the cmdlet associates the target type with the tenant.

The acceptable values for this parameter are:

-- Groups
-- Users
-- ServicePrincipals
-- Applications
-- Devices

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 
Accepted values: Groups, Users, ServicePrincipals, Applications, Devices

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolSettings](22a5d63b-5386-4137-965f-e5cf5696dde5)

[New-MsolSettings](2fe0b98e-77b0-4122-a5d0-3ed553f83b36)

[Remove-MsolSettings](79972530-7187-4e7d-96ba-0c5351e4adde)

