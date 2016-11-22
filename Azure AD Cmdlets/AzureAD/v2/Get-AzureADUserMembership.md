---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserMembership

## SYNOPSIS
Get user memberships.

## SYNTAX

```
Get-AzureADUserMembership -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the memberships of a given user
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUserMembership  -ObjectId $UserId

Output: 


ObjectId                             ObjectType
--------                             ----------
019ea7a2-1613-47c9-81cb-20ba35b1ae48 Role
ef58cdc0-3e08-4e02-ab16-db99ef8dfa49 Group
52b94dfa-293a-496c-b98e-e16a20247065 Group
a7cf942b-248c-4bec-9f52-f1a6493959c4 Group
31dba078-ade5-4f97-ac38-3b2edb1af6e0 Group
8c6a5c45-e93e-4f2b-81be-b57ad4c43ddd Role
d96eb2b3-0970-4827-8f26-6008efd86511 Role
9c2564d6-e4d7-4167-a79f-4b961512f232 Group
36db8aaf-022a-448d-aedc-34ef2ceb943c Group
0e6cf869-82ca-4647-b330-420b9a6f8ef7 Group
78045c26-218e-46fb-94b6-1a47320da153 Group
093fc0e2-1d6e-4a1b-9bf8-effa0196f1f7 Group
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

