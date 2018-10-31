---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: C38ED8D1-68B3-4D78-8386-20F6FC87A167
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolRoleMember

## SYNOPSIS
Gets members of a role.

## SYNTAX

### ListRoleMembers__0 (Default)
```
Get-MsolRoleMember [-RoleObjectId <Guid>] [-MemberObjectTypes <String[]>] [-SearchString <String>]
 [-MaxResults <Int32>] [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolRoleMember [-RoleObjectId <Guid>] [-MemberObjectTypes <String[]>] [-SearchString <String>] [-All]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolRoleMember** cmdlet gets members of the specified role.

## EXAMPLES

### Example 1: Get members of a role
```
PS C:\> $RoleMembers = Get-MsolRole -RoleName "Company Administrator"
```

This command returns all the members of the specified role.
The command stores the results in the $RoleMembers variable.

## PARAMETERS

### -All
Indicates that this cmdlet returns all results that it finds.
Do not specify this parameter and the _MaxResults_ parameter.

```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.
The default value is 250.

```yaml
Type: Int32
Parameter Sets: ListRoleMembers__0
Aliases:

Required: False
Position: Named
Default value: 250
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
Specifies the unique ID of the role from which to remove members.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
Specifies a string.
This cmdlet returns objects with a display name or email address that start with this string.
The string to search on.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -MemberObjectTypes
Specifies an array of member object types.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administation.RoleMember
This cmdlet returns role member objects that contain the following information:

* DisplayName. The display name of the role member.

* EmailAddress. The email address of the role member.

* IsLicensed. Whether or not the user is licensed.

* LastDirSyncTime. The date and time that this member was last synced.

* ObjectId. The unique ID of the member.

* OverallProvisioningStatus. The provisioning status of this user.

* RoleMemberType. The type of role member.
Currently only "User" is supported.

* ValidationStatus. Whether or not there are any errors with this group member.

## NOTES

## RELATED LINKS
[Add-MsolRoleMember](./Add-MsolRoleMember.md)

[Remove-MsolRoleMember](./Remove-MsolRoleMember.md)
