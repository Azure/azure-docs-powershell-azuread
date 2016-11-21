---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserCreatedObject

## SYNOPSIS
Get objects created by the user.

## SYNTAX

```
Get-AzureADUserCreatedObject -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the objects that are created by a given user
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUserCreatedObject -ObjectId $UserId

Output:


ObjectId                             ObjectType 
--------                             ---------- 
f618e073-cda3-4fc7-b8bd-5ad63f19840f ServicePrincipal 
ed70f968-38ec-48d6-ae58-decfe80bfd5f ServicePrincipal 
35ab4659-f61c-4a75-98d2-ef1d04ac2095 ServicePrincipal 
d0ce9d42-c943-43a1-a0b0-b1ded8d0ce3d ServicePrincipal
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

