---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 8212C7A5-3AA7-4E28-9F0C-D0C97F8AC08E
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
PS C:\>Get-AzureADGroupMember -ObjectId "62438306-7c37-4638-a72d-0ee8d9217680"

ObjectId                             ObjectType
--------                             ----------
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 User
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADGroupMember](./Add-AzureADGroupMember.md)
[Remove-AzureADGroupMember](./Remove-AzureADGroupMember.md)

