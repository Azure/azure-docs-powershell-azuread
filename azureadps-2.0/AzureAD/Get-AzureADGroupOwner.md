---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADGroupOwner

## SYNOPSIS
Gets an owner of a group.

## SYNTAX

```
Get-AzureADGroupOwner -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADGroupOwner cmdlet gets an owner of a group in the Microsoft Entra ID.

## EXAMPLES

### Example 1: Get a group owner by ID
```
PS C:\>Get-AzureADGroupOwner -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"

ObjectId                             ObjectType
--------                             ----------
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 User
```

This command gets the specified group owner.

## PARAMETERS

### -All
If true, return all group owners.
If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a group in the Microsoft Entra ID.

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

See the [migration guide for Get-AzureADGroupOwner](./migrate/Get-AzureADGroupOwner.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Add-AzureADGroupOwner](Add-AzureADGroupOwner.md)

[Remove-AzureADGroupOwner](Remove-AzureADGroupOwner.md)
