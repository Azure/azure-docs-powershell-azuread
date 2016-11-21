---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalPasswordCredential

## SYNOPSIS
Get a service principal's password credentials

## SYNTAX

```
Get-AzureADServicePrincipalPasswordCredential -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve the password credential of a give Service Principal
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
Get-AzureADServicePrincipalPasswordCredential -ObjectId $ServicePrincipalId
```

## PARAMETERS

### -ObjectId
The objectID of the application for which to get the password credential

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

