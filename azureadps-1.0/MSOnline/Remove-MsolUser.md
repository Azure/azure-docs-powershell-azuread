---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: CF0916CC-7239-438D-87F7-BF39B733B77F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolUser

## SYNOPSIS
Removes a user from Azure Active Directory.

## SYNTAX

### RemoveUser__0 (Default)
```
Remove-MsolUser -ObjectId <Guid> [-RemoveFromRecycleBin] [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveUserByUpn__0
```
Remove-MsolUser [-RemoveFromRecycleBin] [-Force] -UserPrincipalName <String> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolUser** cmdlet is used to remove a user from Azure Active Directory.
This cmdlet deletes the user, their licenses, and any other associated data.

## EXAMPLES

### Example 1: Remove a user
```
Remove-MsolUser -UserPrincipalName "davidchew@contoso.com"
```

This command removes the user davidchew@contoso.com from Azure Active Directory.
If the user has any licenses, the cmdlet removes these.
The command prompts you to confirm the operation.

### Example 2: Remove a user without confirmation
```
Remove-MsolUser -UserPrincipalName "davidchew@contoso.com" -Force
```

This command removes davidchew@contoso.com from Azure Active Directory.
If the user has any licenses, the cmdlet removes these.

### Example 3: Remove a user from the Recycle Bin
```
Remove-MsolUser -UserPrincipalName "davidchew@contoso.com" -RemoveFromRecycleBin
```

This command removes davidchew@contoso.com from the Azure Active Directory recycle bin.
The command prompts you to confirm the operation.
This command permanently removes the user.

## PARAMETERS

### -Force
Indicates that this cmdlet does not prompt you for confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the user to remove.

```yaml
Type: Guid
Parameter Sets: RemoveUser__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemoveFromRecycleBin
Indicates that this cmdlet permanently removes a deleted user from the recycle bin.
This operation which can be applied only to deleted users.
When this operation has been completed, you will not be able to recover the user by using the [Restore-MsolUser](./Restore-MsolUser.md) cmdlet.

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
Specifies the user principal name of the user to remove.

```yaml
Type: String
Parameter Sets: RemoveUserByUpn__0
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
[Get-MsolUser](./Get-MsolUser.md)

[New-MsolUser](./New-MsolUser.md)

[Restore-MsolUser](./Restore-MsolUser.md)

[Set-MsolUser](./Set-MsolUser.md)
