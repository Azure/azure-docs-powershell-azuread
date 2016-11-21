---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADContactManager

## SYNOPSIS
Retrieves the manager of a contact from Azure Active Directory

## SYNTAX

```
Get-AzureADContactManager -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Get the manager of a Contact
```
$Contact = Get-AzureADContact -top 1
Get-AzureADContactManager -ObjectId $Contact.ObjectId
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

