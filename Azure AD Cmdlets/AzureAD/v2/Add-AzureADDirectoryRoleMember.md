---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADDirectoryRoleMember

## SYNOPSIS
Add a member to a directory role

## SYNTAX

```
Add-AzureADDirectoryRoleMember -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add a user to a directory role
```
$Role = Get-AzureADDirectoryRole
$User = get-azureaduser -top 1
Add-AzureADDirectoryRoleMember  -ObjectId $Role[0].ObjectId -RefObjectId $User.ObjectId
```

## PARAMETERS

### -ObjectId
The unique identifier of a directory role in Azure Active Directory (ObjectId)

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

