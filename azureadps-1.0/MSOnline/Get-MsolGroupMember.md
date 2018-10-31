---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 15A181E5-32EA-4DAB-942D-2DDCF1C71140
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolGroupMember

## SYNOPSIS
Retrieves members of the specified group.

## SYNTAX

### ListGroupMembers__0 (Default)
```
Get-MsolGroupMember [-GroupObjectId <Guid>] [-MemberObjectTypes <String[]>] [-SearchString <String>]
 [-MaxResults <Int32>] [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolGroupMember [-GroupObjectId <Guid>] [-MemberObjectTypes <String[]>] [-SearchString <String>] [-All]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolGroupMember** cmdlet gets members of the specified group.
The members can be either users or groups.

## EXAMPLES

### Example 1: Get all members of a group
```
PS C:\> Get-MsolGroupMember -GroupObjectId 74d7b44e-6811-4250-bffe-8292e3b0b689
```

This command retrieves all members of the specified group.
The members can be users or groups.

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

### -GroupObjectId
Specifies the unique ID of the group from which to get members.

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

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.
The default value is 250.

```yaml
Type: Int32
Parameter Sets: ListGroupMembers__0
Aliases:

Required: False
Position: Named
Default value: 250
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
Specifies a string.
This cmdlet returns objects with a display name or email address that start with this string.

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

### Microsoft.Online.Administration.GroupMember
This cmdlet returns objects that contain the following information:

* CommonName. The common name of the group.

* DisplayName. The display name of the group.

* EmailAddress. The primary email address of the group (for MailEnabled groups only).

* GroupMemberType. The group type (SecurityGroup, Distributionlist, or MailEnabledSecurityGroup).

* ObjectId. The unique ID of the group.

## NOTES

## RELATED LINKS
[Add-MsolGroupMember](./Add-MsolGroupMember.md)

[Remove-MsolGroupMember](./Remove-MsolGroupMember.md)
