---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADUserExtension

## SYNOPSIS
Removes a user extension.

## SYNTAX

### SetSingle
```
Remove-AzureADUserExtension -ObjectId <String> -ExtensionName <String> [<CommonParameters>]
```

### SetMultiple
```
Remove-AzureADUserExtension -ObjectId <String>
 -ExtensionNames <System.Collections.Generic.List`1[System.String]> [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADUserExtension cmdlet removes a user extension from Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Remove-AzureADUserExtension -ObjectId TestUser@example.com -ExtensionName "Test Extension"
```

This will remove the "Test Extension" attribute from user: TestUser@example.com.

## PARAMETERS

### -ExtensionName
Specifies the name of an extension.

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

### -ExtensionNames
Specifies an array of extension names.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetMultiple
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies an object ID.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUserExtension]()

[Set-AzureADUserExtension]()

