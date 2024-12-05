---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: DD253761-F1BB-4EF1-B0CB-586C0040DECE
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADDirectoryRoleMember

## SYNOPSIS
Gets members of a directory role.

## SYNTAX

```
Get-AzureADDirectoryRoleMember -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDirectoryRoleMember** cmdlet gets the members of a directory role in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get members by role ID
```
PS C:\>Get-AzureADDirectoryRoleMember -ObjectId "67efd1ad-1046-4fb8-bb57-1d2e4f66c74e"

ObjectId                             ObjectType
--------                             ----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb User
bbbbbbbb-1111-2222-3333-cccccccccccc User
cccccccc-2222-3333-4444-dddddddddddd User
```

This command gets the members of the specified role.

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
Specifies the ID of a directory role in Azure AD.

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

[Add-AzureADDirectoryRoleMember](./Add-AzureADDirectoryRoleMember.md)
[Remove-AzureADDirectoryRoleMember](./Remove-AzureADDirectoryRoleMember.md)
