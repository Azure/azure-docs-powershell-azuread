---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 54F95D25-05CB-4AC9-A11A-4BF3E734CA4F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolRoleMember

## SYNOPSIS
Removes a member from an administrator role.

## SYNTAX

### RemoveRoleMembers__0 (Default)
```
Remove-MsolRoleMember -RoleObjectId <Guid> [-RoleMemberType <RoleMemberType>] [-RoleMemberObjectId <Guid>]
 [-RoleMemberEmailAddress <String>] [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveRoleMembersByRoleName__0
```
Remove-MsolRoleMember [-RoleMemberType <RoleMemberType>] [-RoleMemberObjectId <Guid>]
 [-RoleMemberEmailAddress <String>] -RoleName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolRoleMember** cmdlet removes a user from an administrator role.

## EXAMPLES

### Example 1: Remove a member from an administrator role
```
PS C:\> Remove-MsolRoleMember -RoleName "Company Administrator" -RoleMemberType User -RoleMemberEmailAddress "elisadaugherty@contoso.com"
```

This command removes elisadaugherty@contoso.com from the Company Administrator role.

## PARAMETERS

### -RoleMemberEmailAddress
Specifies the member remove add.
Specify either the _RoleMemberEmailAddress_ or _RoleMemberObjectId_ parameter.

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

### -RoleMemberObjectId
Specifies the unique object ID of the member to remove.
Specify either _RoleMemberEmailAddress_ or _RoleMemberObjectId_.

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

### -RoleMemberType
Specifies the type of role of the member to remove.

```yaml
Type: RoleMemberType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleName
Specifies the name of the role from which to remove members.
Specify either the _RoleName_ or _RoleObjectId_ parameter.

```yaml
Type: String
Parameter Sets: RemoveRoleMembersByRoleName__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
Specifies the unique ID of the role from which to remove members.
Specify either _RoleName_ or _RoleObjectId_.

```yaml
Type: Guid
Parameter Sets: RemoveRoleMembers__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
[Add-MsolRoleMember](./Add-MsolRoleMember.md)

[Get-MsolRoleMember](./Get-MsolRoleMember.md)
