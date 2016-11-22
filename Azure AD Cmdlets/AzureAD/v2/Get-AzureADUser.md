---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUser

## SYNOPSIS
Retrieves a specific user from Azure Active Directory

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-AzureADUser [-Top <Nullable`1[Int32]>] [-Filter <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-AzureADUser [-SearchString <String>]
```

### UNNAMED_PARAMETER_SET_3
```
Get-AzureADUser -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Get 10 users from your directory
```
Get-AzureADUser -Top 10
```

Return users from tenant that meets the requirement.

### Retrieve a specific user from the directory, search by Object Id
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUser -ObjectId $UserId
```

Return the specific user using user's Object Id.

### Retrieve users from the directory, search with a search string
```
Get-AzureADUser -SearchString "New"

ObjectId                             DisplayName UserPrincipalName                   UserType
--------                             ----------- -----------------                   --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    NewUser@drumkit.onmicrosoft.com     Member
2b450b8e-1db6-42cb-a545-1b05eb8a358b New user    NewTestUser@drumkit.onmicrosoft.com Member
```

This cmdlet will return all users where the text provided in the -SearchString parameter appear the first characters in the DisplayName or userPrincipalName

## PARAMETERS

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Filter
The filter parameter can be used to filter returned objects of a cmdlet using an Odata filter statement.
An example would be 

Get-AzureADUser -Filter "DisplayName eq 'TestName'"

which would only return user objects for which the DisplayName equals "TestName".

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
The SearchString parameter allows you to search for specific objects.
This includes the DisplayName and Description attribute as well as addtional string attributes for an object

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The unique identifier of a user in Azure Active Directory (UPN or ObjectId)

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_3
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

