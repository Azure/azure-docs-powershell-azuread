---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: DFEF698C-93D2-4D67-A8B2-4A1D3ADDCBBA
online version: 
schema: 2.0.0
---

# Set-AzureADUserExtension

## SYNOPSIS
Sets a user extension.

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
The **Set-AzureADUserExtension** cmdlet sets a user extension in Azure Active Directory (Azure AD).

## EXAMPLES

### Example 1: Set the value of an extension attribute for a user
```
PS C:\> $User = Get-AzureADUser -Top 1
PS C:\> Set-AzureADUserExtension -ObjectId $User.ObjectId -ExtensionName extension_e5e29b8a85d941eab8d12162bd004528_extensionAttribute8 -ExtensionValue "New Value"
```

The first command gets a user by using the [Get-AzureADUser](./Get-AzureADUser.md) cmdlet, and then stores it in the $User variable.

The second command  sets the value of the extension attribute that hast he specified name to the value New Value.
You can get extension attribute names by using the [Get-AzureAdExtensionProperty](./Get-AzureAdExtensionProperty.md) cmdlet.

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

### -ExtensionNameValues
Specifies extension name values.
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
Specifies an extension value.
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
Specifies the ID of an object.
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

[Get-AzureADUser](./Get-AzureADUser.md)

[Get-AzureADUserExtension](./Get-AzureADUserExtension.md)

[Get-AzureAdExtensionProperty](./Get-AzureAdExtensionProperty.md)

[Remove-AzureADUserExtension](./Remove-AzureADUserExtension.md)
