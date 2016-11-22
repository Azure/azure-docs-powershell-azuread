---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDirectoryRoleMember

## SYNOPSIS
Get the members of a directory role.

## SYNTAX

```
Get-AzureADDirectoryRoleMember -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve the members of a role
```
$Roles = Get-AzureADDirectoryRole
Get-AzureADDirectoryRoleMember -ObjectId $Roles[0].ObjectId


Output:

ObjectId                             ObjectType
--------                             ----------
ba6752c4-6a2e-4be5-a23d-67d8d5980796 User
df19e8e6-2ad7-453e-87f5-037f6529ae16 User
c13dd34a-492b-4561-b171-40fcce2916c5 User
0558a23b-438a-48aa-8e30-5042e0746f69 User
1fbae2b2-bb4b-48f9-bb38-83e9e1ad4bff User
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

