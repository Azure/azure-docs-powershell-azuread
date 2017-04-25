---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
ms.assetid: F1CEBDF4-5AF8-4AFC-AA1F-D36CEC381D04
online version: 
schema: 2.0.0
---

# Get-AzureADObjectSetting

## SYNOPSIS
Gets an object setting.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADObjectSetting -TargetType <String> -TargetObjectId <String> [-All <Boolean>] [-Top <Int32>]
 [<CommonParameters>]
```

### GetById
```
Get-AzureADObjectSetting -TargetType <String> -TargetObjectId <String> -Id <String> [-All <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADObjectSetting cmdlet gets an object setting from Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -All
If true, return all objects settings. If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
Specifies the ID of a settings object. 

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetObjectId
Specifies the ID of the target object.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TargetType
Specifies the target type. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
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

[New-AzureADObjectSetting](./New-AzureADObjectSetting.md)

[Remove-AzureADObjectSetting](./Remove-AzureADObjectSetting.md)

[Set-AzureADObjectSetting](./Set-AzureADObjectSetting.md)

