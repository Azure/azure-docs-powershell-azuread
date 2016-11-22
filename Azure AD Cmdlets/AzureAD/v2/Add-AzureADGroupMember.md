---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADGroupMember

## SYNOPSIS
Add a member to a group

## SYNTAX

```
Add-AzureADGroupMember -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add a user as a member to a group
```
$UserId = (Get-AzureADUser -top 1).ObjectId
$GroupId = (Get-azureADGroup -top 1).ObjectId
Add-AzureADGroupMember -ObjectId $GroupId -RefObjectId ObjectId
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
The unique identifier of the specific Azure Active Directory object that will be assigned as member

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

