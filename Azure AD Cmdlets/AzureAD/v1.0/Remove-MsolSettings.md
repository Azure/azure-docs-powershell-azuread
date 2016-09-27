---
external help file: AzureADHelpMSOL.xml
online version: 4955285a-6fe5-46e2-affc-8b1798ae8f2a
schema: 2.0.0
---

# Remove-MsolSettings

## SYNOPSIS
Removes a directory setting.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Remove-MsolSettings -SettingId <String>
```

### UNNAMED_PARAMETER_SET_2
```
Remove-MsolSettings [-SettingId <String>] [-TargetObjectId <String>] [-TargetType]
```

## DESCRIPTION
The **Remove-MsolSettings** cmdlet removes a directory setting.

## EXAMPLES

### Example 1: Remove a directory setting
```
PS C:\>Remove-MsolServicePrincipalCredential -SettingId "4197A724-04F3-456F-B42E-2B830C5D8152"
```

This command removes a directory setting with the specified setting ID.

### Example 2: Remove a directory setting with a specified target object ID
```
PS C:\>Remove-MsolServicePrincipalCredential -SettingId "4197A724-04F3-456F-B42E-2B830C5D8152" -TargetType Groups -TargetObjectId "Group002"
```

This command removes a directory setting associated with a group object.

## PARAMETERS

### -SettingId
Specifies the directory setting to be removed.
You can use the Get-MsolAllSettings cmdlet to get the setting ID for a directory setting.

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

## NOTES

## RELATED LINKS

[Get-MsolAllSettings](4955285a-6fe5-46e2-affc-8b1798ae8f2a)

[New-MsolSettings](2fe0b98e-77b0-4122-a5d0-3ed553f83b36)

[Set-MsolSettings](31e47047-4159-488c-9c8a-ed3369268375)

