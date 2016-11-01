---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 22A5D63B-5386-4137-965F-E5CF5696DDE5
---

# Get-MsolSettings

## SYNOPSIS
Gets a directory setting.

## SYNTAX

### None (Default)
```
Get-MsolSettings -SettingId <String> [<CommonParameters>]
```

### Scope
```
Get-MsolSettings [-TargetType <TargetType>] [-TargetObjectId <String>] [-SettingId <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolSettings** cmdlet gets a directory setting.

## EXAMPLES

### Example 1: Get a directory setting using a setting ID
```
PS C:\>Get-MsolSettings -SettingId "4197A724-04F3-456F-B42E-2B830C5D8152"
```

This command gets a directory setting associated with the specified setting ID.

### Example 2: Get a directory setting using a target group ID with a specific target type
```
PS C:\>Get-MsolSettings -SettingId "4197A724-04F3-456F-B42E-2B830C5D8152" -TargetType Groups -TargetObjectId "Group011"
```

This command gets a directory setting associated with the specified setting ID that belongs to the target type Groups that has the target object ID named Group011.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Setting
This cmdlet returns a directory setting object that contains the following information: 

- DisplayName: The name of the setting. 
- TemplateId: The unique ID of the directory setting template this setting belongs to. 
- Id: The unique string ID of the directory setting.
This value should be used when updating setting. 
- Values: The name value pair that describes settings detail.

## NOTES

## RELATED LINKS

[Get-MsolAllSettings](./Get-MsolAllSettings.md)

[Get-MsolSettingTemplate](./Get-MsolSettingTemplate.md)

[Get-MsolAllSettingTemplate](./Get-MsolAllSettingTemplate.md)


