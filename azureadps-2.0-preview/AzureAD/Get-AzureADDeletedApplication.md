---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADDeletedApplication

## SYNOPSIS
Retrieves the list of previously deleted applications

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDeletedApplication [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADDeletedApplication [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves the list of previously deleted applications

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADApplication

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 00001111-aaaa-2222-bbbb-3333cccc4444 PowerShellGraphAPI
bbbbbbbb-1111-2222-3333-cccccccccccc 11112222-bbbb-3333-cccc-4444dddd5555 WingTips
cccccccc-2222-3333-4444-dddddddddddd 22223333-cccc-4444-dddd-5555eeee6666 AzurePopulator


PS C:\WINDOWS\system32> Remove-AzureADApplication -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb
PS C:\WINDOWS\system32> Get-AzureADDeletedApplication

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 00001111-aaaa-2222-bbbb-3333cccc4444 PowerShellGraphAPI
```

This example shows how an existing application was deleted and how the G-AzureADDeletedApplication cmdlet retrieves the application from the list of deleted applications

## PARAMETERS

### -All
If true, return all deleted applications. If false, return the number of objects specified by the Top parameter

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

### -Filter
Retrieve only those deleted applications that satisfy the filter

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Retrieve only those applications that satisfy the -SearchString value

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
The maximum number of applications returned by this cmdlet. the default value is 100.

```yaml
Type: Int32
Parameter Sets: GetQuery
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

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
