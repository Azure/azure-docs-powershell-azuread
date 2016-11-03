---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: A14A0302-406A-4417-AF11-A6CF19B22101
---

# Add-MsolRoleMember

## SYNOPSIS
Adds a member to an existing administrator role.

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
This cmdlet is used to add a member to a role. 
Currently, only Users and ServicePrincipals can be added to a role (adding a security group is not supported).

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Add-MsolRoleMember -RoleName "Company Administrator" -RoleMemberEmailAddress "user@contoso.com"

          None
```

Description

-----------

This command adds user@contoso.com to the Company Administrator role.
To get the list of values for RoleName, use the Get-MsolRole cmdlet.

## PARAMETERS

### -RoleMemberEmailAddress
The object ID of the member to add.
For users, this should be the user ID.
Only users can be added to a role (adding a security group is not supported).
Either RoleMemberEmailAddress or RoleMemberObjectId should be provided.

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
The object ID of the member to add.
Only users can be added to a role (adding a security group is not supported).
Either RoleMemberEmailAddress or RoleMemberObjectId should be provided.

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
The type of role of the member (User, Group or ServicePrincipal) to add. 
Currently only Users and ServicePrincipals can be added to Roles.

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
The name of the role to add members to.
Only users can be added to a role (adding a security group is not supported).
Either RoleName or RoleObjectId should be provided.

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
The role to add members to.
Only users can be added to a role (adding a security group is not supported).
Either RoleName or RoleObjectId should be provided.

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
The unique ID of the tenant to perform the operation on.
If this is not provided, then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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


