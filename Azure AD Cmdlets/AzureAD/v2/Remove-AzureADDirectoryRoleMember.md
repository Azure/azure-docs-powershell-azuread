---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADDirectoryRoleMember

## SYNOPSIS
Removes a specific member from a directory role.

## SYNTAX

```
Remove-AzureADDirectoryRoleMember -ObjectId <String> -MemberId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove a member from a directory role
```
Remove-AzureADDirectoryRoleMember -ObjectId 019ea7a2-1613-47c9-81cb-20ba35b1ae48 -MemberId c13dd34a-492b-4561-b171-40fcce2916c5
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

### -MemberId
The unique identifier of the member

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

