---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 6771683C-F5D9-48C4-9591-DC6692407ACA
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
The Remove-MsolGroupMember cmdlet is used to remove a member from a security group.
This member can be either a user or a group.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
$groupId = Get-MsolGroup -searchString MyGroup
          $userid = get-msoluser -userPrincipalName user@contoso.com
          Remove-MsoLGroupMember -groupObjectId $groupid -GroupMemberType User -groupmemberobjectid $userid
```

Description

-----------

Will remove user@contoso.com from MyGroup.

## PARAMETERS

### -GroupMemberObjectId
The object ID of the member (User or Group) to remove from the group.

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
The type of member (User or Group) to remove from the group.

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
The ID of the group to remove members from.

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


