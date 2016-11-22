---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Update-AzureADSignedInUserPassword

## SYNOPSIS
Updates the password for the signed in user in Azure AD

## SYNTAX

```
Update-AzureADSignedInUserPassword -CurrentPassword <SecureString> -NewPassword <SecureString>
```

## DESCRIPTION

## EXAMPLES

### Update the password of the signed in user
```
Update-AzureADSignedInUserPassword -CurrentPassword (ConvertTo-SecureString -String "P0rsche916" -AsPlainText -Force) -NewPassword (ConvertTo-SecureString -String "P@ssw0rd" -AsPlainText -Force)
```

## PARAMETERS

### -CurrentPassword
The current password of the signed in user

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

### -NewPassword
The new password of the signed in user

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

