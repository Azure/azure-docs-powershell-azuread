---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADContract

## SYNOPSIS
Gets a contract.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADContract [-All <Boolean>] [-Top <Int32>] [-Filter <String>]
```

### GetById
```
Get-AzureADContract -ObjectId <String> [-All <Boolean>]
```

## DESCRIPTION
The Get-AzureADContract cmdlet gets a contract from Azure Active Directory.

## EXAMPLES

### Example 1: Get all contracts in the directory
```
Get-AzureADContract
```

This command gets all contracts in the directory.

## PARAMETERS

### -All
If true, return all contracts.
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
This parameter controls which objects are returned.

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
Specifies the ID of a contract.

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

