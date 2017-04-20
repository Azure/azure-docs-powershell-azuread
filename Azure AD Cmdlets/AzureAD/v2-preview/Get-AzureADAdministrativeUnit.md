---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADAdministrativeUnit

## SYNOPSIS
Gets an administrative unit.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADAdministrativeUnit [-All <Boolean>] [-Top <Int32>] [-Filter <String>]
```

### GetById
```
Get-AzureADAdministrativeUnit -ObjectId <String> [-All <Boolean>]
```

## DESCRIPTION
The Get-AzureADAdministrativeUnit cmdlet gets an Azure Active Directory administrative unit.

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -All
If true, return all administrative units.
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
Specifies an oData v3.0 filter statement.
This parameter filters which objects are returned.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureADAdministrativeUnit]()

[Remove-AzureADAdministrativeUnit]()

[Set-AzureADAdministrativeUnit]()

