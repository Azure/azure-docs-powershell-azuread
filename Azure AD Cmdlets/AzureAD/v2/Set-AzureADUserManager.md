---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADUserManager

## SYNOPSIS
Updates the user's manager in Azure Active Directory

## SYNTAX

```
Set-AzureADUserManager -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Set the manager of a user
```
$UserID = (Get-AzureADUser -Top 1).ObjectID
$ManagerID = (Get-AzureADUser -Top 1).ObjectID
Set-AzureADUserManager -ObjectId $UserId -RefObjectId $ManagerId
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

### -RefObjectId
The unique identifier of the specific Azure Active Directory object that will be assigned as Manager

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

