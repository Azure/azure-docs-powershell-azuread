---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 441B9A03-B06D-4B67-91F2-09CB78C11330
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationExtensionProperty

## SYNOPSIS
Removes an application extension property.

## SYNTAX

```
Remove-AzureADApplicationExtensionProperty -ObjectId <String> -ExtensionPropertyId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADApplicationExtensionProperty** cmdlet removes an application extension property for an object in Azure Active Directory.

## EXAMPLES

### Example 1: Remove an extension property
```
PS C:\> Remove-AzureADApplicationExtensionProperty -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84" -ExtensionPropertyId "344ed560-f8e7-410e-ab9f-c79df5c36"
```

This command removes the extension property that has the specified ID from an application in Azure Active Directory.

## PARAMETERS

### -ExtensionPropertyId
Specifies the unique ID of the extension property to remove.

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

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique ID of an application in Azure Active Directory.

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

[Get-AzureADApplicationExtensionProperty](./Get-AzureADApplicationExtensionProperty.md)

[New-AzureADApplicationExtensionProperty](./New-AzureADApplicationExtensionProperty.md)
