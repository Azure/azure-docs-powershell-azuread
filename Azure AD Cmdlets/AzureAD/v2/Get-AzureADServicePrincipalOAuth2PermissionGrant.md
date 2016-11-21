---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalOAuth2PermissionGrant

## SYNOPSIS
Get the list of the oAuth2PermissionGrants that a user granted this service principal.

## SYNTAX

```
Get-AzureADServicePrincipalOAuth2PermissionGrant -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the OAuth2 Permission Grants of a given Service Principal
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
Get-AzureADServicePrincipalOAuth2PermissionGrant -ObjectId $ServicePrincipalId
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

