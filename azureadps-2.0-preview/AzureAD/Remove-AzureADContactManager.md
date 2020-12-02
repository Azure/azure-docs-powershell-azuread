---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: CB0C4658-FF1F-46D4-AD62-8C2FA7E72BCA
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Remove-AzureADContactManager

## SYNOPSIS
Removes a contact's manager.

## SYNTAX

```
Remove-AzureADContactManager -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADContactManager** cmdlet removes a contact's manager in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove the manager from a contact
```
PS C:\> $Contact = Get-AzureADContact -Top 1
PS C:\> Remove-AzureADContactManager -ObjectId $Contact.ObjectId
```

The first command gets a contact by using the [Get-AzureADContact](./Get-AzureADContact.md) cmdlet, and then stores it in the $Contact variable.

The second command removes the manager from the contact in $Contact.

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
Specifies the object ID of a contact in Azure AD.

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

[Get-AzureADContactManager](./Get-AzureADContactManager.md)

[Set-AzureADContactManager](./Set-AzureADContactManager.md)
