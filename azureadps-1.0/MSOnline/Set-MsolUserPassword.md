---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: FE736AD3-BE42-47C0-A41A-05E01D1DD7A9
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolUserPassword

## SYNOPSIS
Resets the password for a user.

## SYNTAX

### ResetUserPassword__0 (Default)
```
Set-MsolUserPassword -ObjectId <Guid> [-NewPassword <String>] [-ForceChangePassword <Boolean>]
 [-ForceChangePasswordOnly <Boolean>] [-TenantId <Guid>] [<CommonParameters>]
```

### ResetUserPasswordByUpn__0
```
Set-MsolUserPassword [-NewPassword <String>] [-ForceChangePassword <Boolean>]
 [-ForceChangePasswordOnly <Boolean>] -UserPrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolUserPassword** cmdlet resets the password of a user.
This cmdlet can only be used for users with standard identities.

## EXAMPLES

### Example 1: Reset a password with a random password
```
PS C:\> Set-MsolUserPassword -UserPrincipalName "davidchew@contoso.com" -ForceChangePassword $ture
```

This command resets the password for davidchew@contoso.com.
The cmdlet generates a random password.
The user is required to reset the password on next sign in.

### Example 2: Reset a password
```
PS C:\> Set-MsolUserPassword -UserPrincipalName "davidchew@consoso.com" -NewPassword "pa$$word"
```

This command resets the password for davidchew@contoso.com.
The user will be required to reset the password on next sign in.

## PARAMETERS

### -ForceChangePassword
Indicates whether the user must change the password the next time they sign in.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NewPassword
Specifies a new password for the user.
If the user is set to require a strong password, then all of the following rules must be met:

* The password must contain at least one lowercase letter
* The password must contain at least one uppercase letter
* The password must contain at least one non-alphanumeric character
* The password cannot contain any spaces, tabs, or line breaks
* The length of the password must be 8-16 characters
* The user name cannot be contained in the password

If you do not specify a password, the cmdlet generates a random password for the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique ID of the user for which to set the password.

```yaml
Type: Guid
Parameter Sets: ResetUserPassword__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Specifies the user principal name of the user for which to set the password.

```yaml
Type: String
Parameter Sets: ResetUserPasswordByUpn__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePasswordOnly


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[Set-MsolUserLicense](./Set-MsolUserLicense.md)

[Set-MsolUserPrincipalName](./Set-MsolUserPrincipalName.md)
