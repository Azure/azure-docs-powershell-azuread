---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADApplicationOwner

## SYNOPSIS
Add an owner to an application

## SYNTAX

```
Add-AzureADApplicationOwner -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add an owner to an application
```
$App = Get-AzureADApplication -Top 1
$Owner = Get-AzureADUser -Top 1
Add-AzureADApplicationOwner -ObjectId $App -RefObjectId $Owner
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

