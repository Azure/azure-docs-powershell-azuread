---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 79972530-7187-4E7D-96BA-0C5351E4ADDE
---

# Remove-MsolSettings

## SYNOPSIS
Removes a directory setting.

## SYNTAX

### None (Default)
```
Remove-MsolSettings -SettingId <String> [<CommonParameters>]
```

### Scope
```
Remove-MsolSettings [-TargetType <TargetType>] [-TargetObjectId <String>] [-SettingId <String>]
 [<CommonParameters>]
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolAllSettings](./Get-MsolAllSettings.md)

[New-MsolSettings](./New-MsolSettings.md)

[Set-MsolSettings](./Set-MsolSettings.md)


