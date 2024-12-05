---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: 8212C7A5-3AA7-4E28-9F0C-D0C97F8AC08E
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADGroupMember

## SYNOPSIS
Gets a member of a group.

## SYNTAX

```
Get-AzureADGroupMember -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADGroupMember** cmdlet gets a member of a group in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a group member by ID
```
PS C:\>Get-AzureADGroupMember -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"

ObjectId                             ObjectType
--------                             ----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb User
```

## PARAMETERS

### -All
If true, return all group members. If false, return the number of objects specified by the Top parameter

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

### -ObjectId
Specifies the ID of a group in Azure AD.

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
Parameter Sets: (All)
Aliases:

Required: False
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

[Add-AzureADGroupMember](./Add-AzureADGroupMember.md)
[Remove-AzureADGroupMember](./Remove-AzureADGroupMember.md)
