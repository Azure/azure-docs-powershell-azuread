---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalKeyCredential

## SYNOPSIS
Get a service principal's key credentials

## SYNTAX

```
Get-AzureADServicePrincipalKeyCredential -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve a Service Principal's key credential
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
Get-AzureADServicePrincipalKeyCredential -ObjectId $ServicePrincipalId
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

