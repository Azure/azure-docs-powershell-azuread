---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADUserPassword

## SYNOPSIS
Sets the password of a user in Azure AD

## SYNTAX

```
Set-AzureADUserPassword -ObjectId <String> -Password <SecureString> [-ForceChangePasswordNextLogin <Boolean>]
```

## DESCRIPTION

## EXAMPLES

### Set the password for a user
```
$UserId = (get-azureadUser -top 1).objectId
Set-AzureADUserPassword -ObjectId $UserId -Password (ConvertTo-SecureString -String "P0rsche916" -AsPlainText -Force)
```

## PARAMETERS

### -ObjectId
@{Text=}

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

### -Password
@{Text=}

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePasswordNextLogin
@{Text=}

```yaml
Type: Boolean
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

