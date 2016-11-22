---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADServicePrincipalOwner

## SYNOPSIS
Add an owner to a service principal

## SYNTAX

```
Add-AzureADServicePrincipalOwner -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add a user as an owner to a service principal
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -top 1).ObjectId
$OwnerId = (Get-azureADUser -top 1).ObjectId
Add-AzureADServicePrincipalOwner -ObjectId $ServicePrincipalId -RefObjectId -$OwnerId
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

### -RefObjectId
The unique identifier of the specific Azure Active Directory object that will be assigned as owner

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

