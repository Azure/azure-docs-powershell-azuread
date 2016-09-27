---
external help file: AzureADHelpMSOL.xml
online version: 4955285a-6fe5-46e2-affc-8b1798ae8f2a
schema: 2.0.0
---

# Get-MsolSettings

## SYNOPSIS
Gets a directory setting.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-MsolSettings -SettingId <String>
```

### UNNAMED_PARAMETER_SET_2
```
Get-MsolSettings [-SettingId <String>] [-TargetObjectId <String>] [-TargetType]
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

### Microsoft.Online.Administration.Setting
This cmdlet returns a directory setting object that contains the following information: 

-- DisplayName: The name of the setting. 
-- TemplateId: The unique ID of the directory setting template this setting belongs to. 
-- Id: The unique string ID of the directory setting.
This value should be used when updating setting. 
-- Values: The name value pair that describes settings detail.

## NOTES

## RELATED LINKS

[Get-MsolAllSettings](4955285a-6fe5-46e2-affc-8b1798ae8f2a)

[Get-MsolSettingTemplate](4a83b1b7-7b08-4983-9e41-bd873f8db2f8)

[Get-MsolAllSettingTemplate](0f14f9f7-1780-4cb2-9362-415a361463be)

