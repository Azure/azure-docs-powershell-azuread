---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADContact

## SYNOPSIS
Retrieves a specific contact from Azure Active Directory

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-AzureADContact [-Top <Nullable`1[Int32]>] [-Filter <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-AzureADContact -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieves all contact objects in the directory
```
Get-AzureADContact

ObjectId                             Mail               DisplayName
--------                             ----               -----------
b052db07-e7ec-4c0e-b481-a5ba550b9ee7 contact@person.com Contact Person
```

## PARAMETERS

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Filter
The filter parameter can be used to filter returned objects of a cmdlet using an Odata filter statement.
An example would be 

Get-AzureADContact -Filter "DisplayName eq 'Mr.
Contact'"

which would only return contact objects for which the DisplayName equals "Mr.
Contact".

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The unique identifier of a contact in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

