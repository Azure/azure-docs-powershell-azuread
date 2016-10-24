---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: ./Get-MsolSettings.md
schema: 2.0.0
ms.assetid: 31E47047-4159-488C-9C8A-ED3369268375
---

# Set-MsolSettings

## SYNOPSIS
Updates a directory setting in Azure Active Directory.

## SYNTAX

### None (Default)
```
Set-MsolSettings -SettingId <String> -SettingsValue <SettingsValue> [<CommonParameters>]
```

### Scope
```
Set-MsolSettings [-TargetType <TargetType>] [-TargetObjectId <String>] [-SettingId <String>]
 [-SettingsValue <SettingsValue>] [<CommonParameters>]
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

### -TargetType
Specifies the object type that settings objects are associated with.
If you do not specify a value, the cmdlet associates the target type with the tenant.

The acceptable values for this parameter are:

- Groups
- Users
- ServicePrincipals
- Applications
- Devices

```yaml
Type: TargetType
Parameter Sets: Scope
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetObjectId
Specifies the object ID that settings objects are associated with.
If you do not specify a value, this cmdlet associates the directory setting with the tenant.

```yaml
Type: String
Parameter Sets: Scope
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SettingId
Specifies the setting ID associated with the directory setting that this cmdlet gets.

```yaml
Type: String
Parameter Sets: None
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Scope
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SettingsValue
Specifies the directory setting value that this cmdlet updates the existing setting with.
This operation overwrites the existing setting.

```yaml
Type: SettingsValue
Parameter Sets: None
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: SettingsValue
Parameter Sets: Scope
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

[Get-MsolSettings](./Get-MsolSettings.md)

[New-MsolSettings](./New-MsolSettings.md)

[Remove-MsolSettings](./Remove-MsolSettings.md)


