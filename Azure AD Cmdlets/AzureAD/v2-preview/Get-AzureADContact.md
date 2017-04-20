---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 393B2C82-CB87-4892-872E-6E6285DFF955
online version: 
schema: 2.0.0
---

# Get-AzureADContact

## SYNOPSIS
Gets a contact from Azure Active Directory.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADContact [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADContact -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADContact** cmdlet gets a contact from Azure Active Directory.

## EXAMPLES

### Example 1 Retrieve all contact objects in the directory
```
PS C:\> Get-AzureADContact

ObjectId                             Mail                DisplayName
--------                             ----                -----------
b052db07-e7ec-4c0e-b481-a5ba550b9ee7 contact@contoso.com Contoso Contact
```

This command retrieves all contact objects in the directory.

## PARAMETERS

### -All
If true, return all contacts. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a contact in Azure Active Directory.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-AzureADContact](./Remove-AzureADContact.md)
[Set-AzureADContact](./Set-AzureADContact.md)
