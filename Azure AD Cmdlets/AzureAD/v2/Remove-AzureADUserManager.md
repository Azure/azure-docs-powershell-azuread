---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADUserManager

## SYNOPSIS
Deletes the user's manager in Azure Active Directory

## SYNTAX

```
Remove-AzureADUserManager -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove the manager of a user with the given ObjectId
```
$User = Get-AzureADUser -top 1
Remove-AzureADUserManager -ObjectId $User.ObjectId
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

