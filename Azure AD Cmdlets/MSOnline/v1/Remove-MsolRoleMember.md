---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 54F95D25-05CB-4AC9-A11A-4BF3E734CA4F
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
The Remove-MsolRoleMember cmdlet is used to remove a user from an administrator role.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolRoleMember -RoleName "Company Administrator" -RoleMemberType User -RoleMemberEmailAddress user@contoso.com
```

Description

-----------

Will remove user@contoso.com from the Company Administrator role.

## PARAMETERS

### -RoleMemberEmailAddress
The object ID of the member (User or Group) to remove.
For users, this should be the
            user ID.
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
The object ID of the member (User or Group) to remove.
Either RoleMemberEmailAddress
            or RoleMemberObjectId should be provided.

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
The type of role of the member (User or Group) to remove.

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
The name of the role to remove members from.
Either RoleName or RoleObjectId should be
            provided.

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
The role to remove members from.
Either RoleName or RoleObjectId should be provided.

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
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
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


