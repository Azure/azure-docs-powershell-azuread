---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADGroupOwner

## SYNOPSIS
Removes an owner from a group.

## SYNTAX

```
Remove-AzureADGroupOwner -ObjectId <String> -OwnerId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove an owner from a group
```
Remove-AzureADGroupOwner -ObjectId 62438306-7c37-4638-a72d-0ee8d9217680 -OwnerId 0a1068c0-dbb6-4537-9db3-b48f3e31dd76
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

### -OwnerId
The unique identifier of the owner

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

