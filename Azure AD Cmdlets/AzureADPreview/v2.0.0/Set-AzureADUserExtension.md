---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: DFEF698C-93D2-4D67-A8B2-4A1D3ADDCBBA
---

# Set-AzureADUserExtension

## SYNOPSIS

## SYNTAX

### SetSingle
```
Set-AzureADUserExtension -ObjectId <String> -ExtensionName <String> -ExtensionValue <String>
 [<CommonParameters>]
```

### SetMultiple
```
Set-AzureADUserExtension -ObjectId <String>
 -ExtensionNameValues <System.Collections.Generic.Dictionary`2[System.String,System.String]>
 [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -ExtensionName
```yaml
Type: String
Parameter Sets: SetSingle
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExtensionNameValues
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetMultiple
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExtensionValue
```yaml
Type: String
Parameter Sets: SetSingle
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


