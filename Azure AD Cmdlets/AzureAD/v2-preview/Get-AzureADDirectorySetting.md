---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
ms.assetid: FF1EF8E7-1372-42D8-966C-19FBE9603F5B
online version: 
schema: 2.0.0
---

# Get-AzureADDirectorySetting

## SYNOPSIS
Gets a directory setting.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDirectorySetting [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

### GetById
```
Get-AzureADDirectorySetting -Id <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADDirectorySetting cmdlet gets a directory setting from Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -All
If true, return all directory settings. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a directory in Azure AD.

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

[New-AzureADDirectorySetting](./New-AzureADDirectorySetting.md)
[Remove-AzureADDirectorySetting](./Remove-AzureADDirectorySetting.md)
[Set-AzureADDirectorySetting](./Set-AzureADDirectorySetting.md)

