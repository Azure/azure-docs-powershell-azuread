---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserDirectReport

## SYNOPSIS
Get the user's direct reports.

## SYNTAX

```
Get-AzureADUserDirectReport -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the direct reports of a given user
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUserDirectReport -ObjectId $UserId

Output:


ObjectId                             ObjectType 
--------                             ---------- 
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 User
```

Output:


ObjectId                             ObjectType --------                             ---------- 5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 User

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

