---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
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
421c3f21-22b1-43ea-b438-f00bcad54bd7 f9009add-63a4-4231-9532-9bdc22742922 PowerShellGraphAPI
4862738f-9ce9-4db6-ab55-e185049f4597 d961ff63-d659-42d5-8ca8-908b3bbb79cb WingTips
49a8bc01-2751-450b-a2e8-b4267f609513 10d861e6-90b3-4854-a504-f656aab2a14e AzurePopulator
79592454-dea7-4660-9d91-f1768e5055ac feabcdd1-711a-4d55-ad5e-0d0577aaaa5e analog
9c4fb233-e88c-4a61-acc9-e8fdcb6758dd e5e29b8a-85d9-41ea-b8d1-2162bd004528 Tenant Schema Extension App
a5fd58ca-9f1b-4184-ba7c-2595b5831e21 641e422d-29af-49c9-a24e-c0ee05ff10d5 PowerShellRunner
c4fdf87f-f68e-4859-8bcf-36579b66005e 71715b24-8cdd-432b-a138-86e8ad179274 Woodgrove HR App
d58d399f-56c3-409c-9efc-fdc28a6bd50e 3ad57eaf-2547-4161-81ae-fde64b5e1c0f ExtensionAttributes
e9cfe5ad-c9eb-4cd7-87c2-2a69059aeb69 576ea3a9-3d7f-4bcc-a2b5-2d1a5088075e GraphDirectoryExtension


PS C:\WINDOWS\system32> Remove-AzureADApplication -ObjectId 79592454-dea7-4660-9d91-f1768e5055ac
PS C:\WINDOWS\system32> Get-AzureADDeletedApplication

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
79592454-dea7-4660-9d91-f1768e5055ac feabcdd1-711a-4d55-ad5e-0d0577aaaa5e analog
```

This example shows how an existing application was deleted and how the G-AzureADDeletedApplication cmdlet retrieves the application from the list of deleted applications

## PARAMETERS

### -All
If true, return all deleted applications.
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
The maximum number of applications returned by this cmdlet.
the default value is 100.

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

## NOTES

See the [migration guide for Get-AzureADDeletedApplication](./migrate/Get-AzureADDeletedApplication.md) to the Microsoft Graph PowerShell.

## INPUTS

### System.String
System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]

## OUTPUTS

### System.Object

## RELATED LINKS
