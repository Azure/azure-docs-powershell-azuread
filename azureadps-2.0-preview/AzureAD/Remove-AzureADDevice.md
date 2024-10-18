---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: 5DCD4EAF-A3D8-49CE-8392-A0F3AE61B86C
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Remove-AzureADDevice

## SYNOPSIS
Deletes a device.

## SYNTAX

```
Remove-AzureADDevice -ObjectId <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADDevice** cmdlet removes a device from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove a device
```
PS C:\>Remove-AzureADDevice -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"
```

This command removes the specified device.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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
Specifies the object ID of a device in Azure AD.

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

[Get-AzureADDevice](./Get-AzureADDevice.md)

[New-AzureADDevice](./New-AzureADDevice.md)

[Set-AzureADDevice](./Set-AzureADDevice.md)
