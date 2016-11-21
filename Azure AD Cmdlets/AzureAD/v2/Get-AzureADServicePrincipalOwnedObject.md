---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalOwnedObject

## SYNOPSIS
Get objects owned by the service principal.

## SYNTAX

```
Get-AzureADServicePrincipalOwnedObject -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the owned objects of a given Service Principal
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
Get-AzureADServicePrincipalOwnedObject -ObjectId $ServicePrincipalId
```

## PARAMETERS

### -ObjectId
The unique idenfier of an service principal in Azure Active Directory

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

