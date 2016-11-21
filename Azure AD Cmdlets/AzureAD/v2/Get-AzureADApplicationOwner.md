---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationOwner

## SYNOPSIS
Get owners of an application.

## SYNTAX

```
Get-AzureADApplicationOwner -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the application owner of an application
```
$AppObjectId = (Get-AzureADApplication -top 1).objectId
Get-AzureADApplicationOwner -ObjectId $AppObjectId

Output:

ObjectId                             ObjectType
--------                             ----------
c13dd34a-492b-4561-b171-40fcce2916c5 User
```

## PARAMETERS

### -ObjectId
The unique idenfier of an application in Azure Active Directory

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

