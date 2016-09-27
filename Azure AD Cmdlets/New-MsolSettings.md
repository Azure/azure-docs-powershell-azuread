---
external help file: AzureADHelpMSOL.xml
online version: 22a5d63b-5386-4137-965f-e5cf5696dde5
schema: 2.0.0
---

# New-MsolSettings

## SYNOPSIS
Creates a directory setting.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
New-MsolSettings -SettingsObject <Settings>
```

### UNNAMED_PARAMETER_SET_2
```
New-MsolSettings [-SettingsObject <Settings>] [-TargetObjectId <String>] [-TargetType]
```

## DESCRIPTION
The **New-MsolSettings** cmdlet creates a directory setting.

## EXAMPLES

### Example 1: Add a directory setting
```
PS C:\>$Template = (Get-MsolAllSettingTemplate)[0] 
PS C:\> $Settings = $Template.CreateSettingsObject() New-MsolSetting -SettingsObject $Settings
```

The first command gets all setting templates and stores the results in the variable named $Template.

The second command adds a directory setting stored in the variable named $Settings with default values to the tenant.

### Example 2: Add a directory setting to a specific target type
```
PS C:\>$Template = (Get-MsolAllSettingTemplate)[0] 
PS C:\> $Settings = $template.CreateSettingsObject() New-MsolSetting -SettingsObject $Settings -TargetType Groups -TargetObjectId
```

The first command gets all setting templates and stores the results in the variable named $Template.

The second command adds a directory setting stored in the variable named $Settings with default values to the tenant.
This command adds the settings to the Groups target type.

## PARAMETERS

### -SettingsObject
Specifies the **SettingsObject** that contains necessary information to create a directory setting.

```yaml
Type: Settings
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByValue,ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Settings
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
If you do not specify a value, the cmdlet associates the object ID with the tenant.

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

[Remove-MsolSettings](79972530-7187-4e7d-96ba-0c5351e4adde)

[Set-MsolSettings](31e47047-4159-488c-9c8a-ed3369268375)

