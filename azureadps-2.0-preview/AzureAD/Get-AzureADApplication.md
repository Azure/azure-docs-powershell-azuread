---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: FC0F8815-DEEC-4672-81A1-68A1095E5543
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADApplication

## SYNOPSIS
Gets an application.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADApplication [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADApplication [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADApplication -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADApplication** cmdlet gets an Azure Active Directory application.

## EXAMPLES

### Example 1: Get an application by display name
```
PS C:\>Get-AzureADApplication -Filter "DisplayName eq 'TestName'"

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
3ddd22e7-a150-4bb3-b100-e410dea1cb84 36ee4c6c-0812-40a2-b820-b22ebd02bce3 TestName
```

This command gets an application by its display name.

### Example 2: Get an application by ID
```
PS C:\>Get-AzureADApplication -Filter "AppId eq '00001111-aaaa-2222-bbbb-3333cccc4444'"
```

This command gets an application by its ID.

Output:

    ObjectId                             AppId                                DisplayName
    --------                             -----                                -----------  
    00001111-aaaa-2222-bbbb-3333cccc4444 36ee4c6c-0812-40a2-b820-b22ebd02bce3 MyNewApp

### Retrieve an application by identifierUris
```
Get-AzureADApplication -Filter "identifierUris/any(uri:uri eq 'http://wingtips.wingtiptoysonline.com')"
```

## PARAMETERS

### -All
If true, return all applications. If false, return the number of objects specified by the Top parameter

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
Specifies an oData v3.0 filter statement. This parameter controls which objects are returned.

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

### -ObjectId
Specifies the ID of an application in Azure Active Directory.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.


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
Specifies the maximum number of records to return.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADApplication](./New-AzureADApplication.md)
[Remove-AzureADApplication](./Remove-AzureADApplication.md)
[Set-AzureADApplication](./Set-AzureADApplication.md)
