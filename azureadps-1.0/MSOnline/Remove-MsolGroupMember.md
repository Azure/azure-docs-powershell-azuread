---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 6771683C-F5D9-48C4-9591-DC6692407ACA
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolGroupMember

## SYNOPSIS
Removes a member from a security group.

## SYNTAX

```
Remove-MsolGroupMember -GroupObjectId <Guid> [-GroupMemberType <GroupMemberType>] [-GroupMemberObjectId <Guid>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolGroupMember** cmdlet is used to remove a member from a security group.
This member can be either a user or a group.

## EXAMPLES

### Example 1: Remove a user from a group
```
PS C:\> $GroupId = Get-MsolGroup -SearchString "MyGroup"
PS C:\> $UserId = Get-MsolUser -UserPrincipalName "evannarvaez@contoso.com"
PS C:\> Remove-MsoLGroupMember -GroupObjectId $GroupId -GroupMemberType User -GroupmemberObjectId $UserId
```
This example removes the user evannarvaez@contoso.com from the group named MyGroup.

## PARAMETERS

### -GroupMemberObjectId
Specifies the unique object ID of the user or group to remove from the group.

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

### -GroupMemberType
Specifies the type of member to remove from the group.
Valid values are: User and Group.

```yaml
Type: GroupMemberType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupObjectId
Specifies the unique ID of the group from which to remove members.

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
[Add-MsolGroupMember](./Add-MsolGroupMember.md)

[Get-MsolGroupMember](./Get-MsolGroupMember.md)
