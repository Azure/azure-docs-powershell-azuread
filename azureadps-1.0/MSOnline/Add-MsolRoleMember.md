---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: A14A0302-406A-4417-AF11-A6CF19B22101
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Add-MsolRoleMember

## SYNOPSIS
Adds a member to an administrator role.

## SYNTAX

### AddRoleMembers__0 (Default)
```
Add-MsolRoleMember -RoleObjectId <Guid> [-RoleMemberType <RoleMemberType>] [-RoleMemberObjectId <Guid>]
 [-RoleMemberEmailAddress <String>] [-TenantId <Guid>] [<CommonParameters>]
```

### AddRoleMembersByRoleName__0
```
Add-MsolRoleMember [-RoleMemberType <RoleMemberType>] [-RoleMemberObjectId <Guid>]
 [-RoleMemberEmailAddress <String>] -RoleName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MsolRoleMember** cmdlet is used to add a member to an administrator role.
Currently, only users and service principals can be added to a role.
Adding a security group is not supported.

## EXAMPLES

### Example 1: Add a member to an administrator role
```
PS C:\> Add-MsolRoleMember -RoleName "Company Administrator" -RoleMemberEmailAddress "elisadaugherty@contoso.com"
```

This command adds elisadaugherty@contoso.com to the Company Administrator role.
To get the list of values for the *RoleName* parameter, use the [Get-MsolRole](./Get-MsolRole.md) cmdlet.

## PARAMETERS

### -RoleMemberEmailAddress
Specifies the member to add.
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
Specifies the unique object ID of the member to add.
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
Specifies the type of role of the member to add.
Valid values are: User and ServicePrincipal.
Group is not currently supported.

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
Specifies the name of the role to which to add members.
Specify either the _RoleName_ or _RoleObjectId_ parameter.

```yaml
Type: String
Parameter Sets: AddRoleMembersByRoleName__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
Specifies the unique ID of the role to which to add members.
Specify either _RoleName_ or _RoleObjectId_.

```yaml
Type: Guid
Parameter Sets: AddRoleMembers__0
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
[Get-MsolRole](./Get-MsolRole.md)

[Get-MsolRoleMember](./Get-MsolRoleMember.md)

[Remove-MsolRoleMember](./Remove-MsolRoleMember.md)
