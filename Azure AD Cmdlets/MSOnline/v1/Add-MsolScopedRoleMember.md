---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 23EB4FFD-3A68-47C5-B6A6-C70482B173AF
---

# Add-MsolScopedRoleMember

## SYNOPSIS
Adds a member to an administrative unit-scoped role.

## SYNTAX

```
Add-MsolScopedRoleMember -RoleObjectId <Guid> -AdministrativeUnitObjectId <Guid> [-RoleMemberObjectId <Guid>]
 [-RoleMemberUserPrincipalName <String>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MsolScopedRoleMember** cmdlet adds a member to an administrative unit-scoped role.

## EXAMPLES

### Example 1:
```
PS C:\> $westcoastau = Get-MsolAdministrativeUnit -searchstring "West Coast"
PS C:\> $uaadmin = Get-MsolRole -RoleName "User Account Administrator"
PS C:\> $admin1 = Get-MsolUser -UserPrincipalName "elisadaugherty@contoso.com"
PS C:\> Add-MsolScopedRoleMember -RoleObjectId $uaadmin.ObjectId -AdministrativeUnitObjectId $westcoastau.ObjectId -RoleMemberObjectId $admin1.ObjectId
```

In this example, elisadaugherty@contoso.com is added as a member to the "User Account Administrator" role scoped for administrative unit "West Coast".

## PARAMETERS

### -RoleObjectId
The object ID of the role to add members to.
Only users can be added to a role (adding a security group is not supported).

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUnitObjectId
The object ID of the administrative unit.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleMemberObjectId
The object ID of the member to add to the role scoped to the administrative unit.
For users, this should be the user ID.
Only users can be added to a role (adding a security group is not supported).

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

### -RoleMemberUserPrincipalName
The user principal name of the member to add.
Only users can be added to a role (adding a security group is not supported).

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
