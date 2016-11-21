---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserManager

## SYNOPSIS
Retrieves the manager of a user from Azure Active Directory

## SYNTAX

```
Get-AzureADUserManager -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve the manager of a given user
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUserManager -ObjectId $UserId

Output:


ObjectId                             ObjectType 
--------                             ---------- 
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 User
```

## PARAMETERS

### -ObjectId
The unique identifier of a user in Azure Active Directory (UPN or ObjectId)

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

