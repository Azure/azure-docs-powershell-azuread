---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 74BD0C15-D7F3-40CE-8D53-4C6C8E3BAA5F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Restore-MsolUser

## SYNOPSIS
Restores a deleted user.

## SYNTAX

### RestoreUser__0 (Default)
```
Restore-MsolUser -ObjectId <Guid> [-AutoReconcileProxyConflicts] [-NewUserPrincipalName <String>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### RestoreUserByUpn__0
```
Restore-MsolUser [-AutoReconcileProxyConflicts] [-NewUserPrincipalName <String>] -UserPrincipalName <String>
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Restore-MsolUser** cmdlet restores a user that is in the Deleted users view to its original state.
Deleted users remain in the Deleted users view for 30 days.

## EXAMPLES

### Example 1: Restore a user
```
PS C:\> Restore-MsolUser -UserPrincipalName "davidchew@contoso.com"
```

This command restores the user "davidchew@contoso.com" from the Deleted users container to the Active users container.

### Example 2: Restore a user and remove conflicts
```
PS C:\> Restore-MsolUser -UserPrincipalName "davidchew@contoso.com" -AutoReconcileProxyConflicts
```

This command restores the user davidchew@contoso.com from the Deleted users container to the Active users container, removing any conflicting proxy addresses.
Use this option if restore fails due to proxy conflicts.

### Example 3: Restore a user
```
PS C:\> Restore-MsolUser -UserPrincipalName "davidchew@contoso.com" -NewUserPrincipalName "davidchew02@contoso.com"
```

This command restores the user davidchew@contoso.com from the Deleted users container to the Active users container as davidchew02@contoso.com.
Use this option if restore fails due to a user principal name conflict.

## PARAMETERS

### -AutoReconcileProxyConflicts
Indicates that any proxy addresses that cause conflicts are removed for the user.
Specify this parameter if one or more of the proxy addresses of the user is also used for another active user.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NewUserPrincipalName
Specifies a new user principal name to use when restoring the user.
Specify this parameter if the original user principal name of the user is in use by another active user.

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
Specifies the unique Object ID of the user to restore.

```yaml
Type: Guid
Parameter Sets: RestoreUser__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Specifies the user ID of the user to restore.

```yaml
Type: String
Parameter Sets: RestoreUserByUpn__0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[Get-MsolUser](./Get-MsolUser.md)

[New-MsolUser](./New-MsolUser.md)

[Remove-MsolUser](./Remove-MsolUser.md)

[Set-MsolUser](./Set-MsolUser.md)
