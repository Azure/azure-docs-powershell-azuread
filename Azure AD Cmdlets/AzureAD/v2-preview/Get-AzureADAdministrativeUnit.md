---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
ms.assetid: 46154156-B7D4-40DE-8EC9-760E44110C76
online version: 
schema: 2.0.0
---

# Get-AzureADAdministrativeUnit

## SYNOPSIS
Gets an administrative unit.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADAdministrativeUnit [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADAdministrativeUnit -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADAdministrativeUnit** cmdlet gets an Azure Active Directory administrative unit.

## EXAMPLES

## PARAMETERS

### -All
If true, return all administrative units. If false, return the number of objects specified by the Top parameter

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
Specifies an oData v3.0 filter statement. This parameter filters which objects are returned.

For more information about oData v3.0 filter expressions, see https://msdn.microsoft.com/en-us/library/hh169248%28v=nav.90%29.aspx

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
Specifies the ID of an administrative unit in Azure Active Directory.

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

[New-AzureADAdministrativeUnit](./New-AzureADAdministrativeUnit.md)

[Remove-AzureADAdministrativeUnit](./Remove-AzureADAdministrativeUnit.md)

[Set-AzureADAdministrativeUnit](./Set-AzureADAdministrativeUnit.md)
