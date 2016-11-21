---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADGroupOwner

## SYNOPSIS
Add an owner to a group

## SYNTAX

```
Add-AzureADGroupOwner -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add a user as an owner to a group
```
$GroupID = (Get-AzureADGroup -Top 1).ObjectId
$OwnerID = (Get-AzureADUser -Top 1).ObjectID
Add-AzureADGroupOwner -ObjectId $GroupID -RefObjectId $OwnerID
```

## PARAMETERS

### -ObjectId
The unique identifier of a group in Azure Active Directory (ObjectId)

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

