---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADContactDirectReport

## SYNOPSIS
Get the contact's direct reports.

## SYNTAX

```
Get-AzureADContactDirectReport -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Get the direct reports of a contact
```
$Contact = Get-AzureADContact -top 1
Get-AzureADContactDirectReport -ObjectId $Contact.ObjectId
```

## PARAMETERS

### -ObjectId
The unique identifier of a contact in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

