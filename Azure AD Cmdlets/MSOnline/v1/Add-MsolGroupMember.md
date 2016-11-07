---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: CCADA679-CABC-4B55-A717-DFD43E7A9191
---

# Add-MsolGroupMember

## SYNOPSIS
Adds a member to an existing security group.

## SYNTAX

```
Add-MsolGroupMember -GroupObjectId <Guid> [-GroupMemberType <GroupMemberType>] [-GroupMemberObjectId <Guid>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Add-MsolGroupMember cmdlet is used to add members to a security group.
The new members can be either users or other security groups.

## EXAMPLES

### Example 1: 
```
Add-MsolGroupMember -groupObjectid <id> -groupmemberType "User" -groupMemberObjectId <id>

          None
```

Description

-----------

This command adds a user to a security group.

## PARAMETERS

### -GroupMemberObjectId
The object ID of the member (User or Group) to add to the group.

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
The type of member (User or Group) to add to the group.

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
The ID of the group to add members to.

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


