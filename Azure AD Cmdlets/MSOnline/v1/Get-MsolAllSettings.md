---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: ./Get-MsolSettings.md
schema: 2.0.0
ms.assetid: 4955285A-6FE5-46E2-AFFC-8B1798AE8F2A
---

# Get-MsolAllSettings

## SYNOPSIS
Gets all directory settings object associated with tenant or group/user/service principal/application/device.

## SYNTAX

```
Get-MsolAllSettings [-TargetType <TargetType>] [-TargetObjectId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolAllSettings** cmdlet gets all directory settings object associated with tenant or group/user/service principal/application/device.

## EXAMPLES

### Example 1: Get a list of directory settings
```
PS C:\>Get-MsolAllSettings
```

This command gets a list of directory settings

### Example 2:
```
PS C:\>Get-MsolAllSettings -TargetType Groups -TargetObjectId "Group001"
```

This command gets a list of directory settings associated with groups target type that belong to the target object ID named Group001.

## PARAMETERS

### -TargetType
Specifies the object type that settings objects are associated with, if this value is not specified, this cmdlet associates with tenant.

The acceptable values for this parameter are:

- Groups
- Users
- ServicePrincipals
- Applications
- Devices

```yaml
Type: TargetType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetObjectId
Specifies the object ID that setting objects are associated with, if this value is not specified, the cmdlet associates with tenant.

```yaml
Type: String
Parameter Sets: (All)
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

[Get-MsolAllSettingTemplate](./Get-MsolAllSettingTemplate.md)


