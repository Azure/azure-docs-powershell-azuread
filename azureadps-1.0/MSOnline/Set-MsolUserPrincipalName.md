---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D6A8C6DA-B071-473D-8618-E1618D42024F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolUserPrincipalName

## SYNOPSIS
Changes the user ID for a user.

## SYNTAX

### ChangeUserPrincipalName__0 (Default)
```
Set-MsolUserPrincipalName -ObjectId <Guid> -NewUserPrincipalName <String> [-ImmutableId <String>]
 [-NewPassword <String>] [-TenantId <Guid>] [<CommonParameters>]
```

### ChangeUserPrincipalNameByUpn__0
```
Set-MsolUserPrincipalName -NewUserPrincipalName <String> [-ImmutableId <String>] [-NewPassword <String>]
 -UserPrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolUserPrincipalName** cmdlet changes the User Principal Name, or user ID, of a user.
This cmdlet can be used to move a user between a federated and standard domain, which results in their authentication type changing to that of the target domain.

## EXAMPLES

### Example 1: Rename a user
```
PS C:\> Set-MsolUserPrincipalName -UserPrincipalName "davidc@contoso.com" -NewUserPrincipalName "davidchew@contoso.com"
```

This command renames davidc@contoso.com to davidchew@contoso.com.

## PARAMETERS

### -ImmutableId
Specifies the immutable ID of the user's federated identity.
This is required if moving the user from a standard to a federated identity domain.

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

### -NewPassword
Specifies the new password for the user.
This is required if moving the user from a federated to a standard identity domain.

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

### -NewUserPrincipalName
Specifies the new user ID of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the user to update.

```yaml
Type: Guid
Parameter Sets: ChangeUserPrincipalName__0
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
Specifies the original user ID of the user to update.

```yaml
Type: String
Parameter Sets: ChangeUserPrincipalNameByUpn__0
Aliases:

Required: True
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

[Set-MsolUserPassword](./Set-MsolUserPassword.md)
