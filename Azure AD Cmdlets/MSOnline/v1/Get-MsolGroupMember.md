---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 15A181E5-32EA-4DAB-942D-2DDCF1C71140
---

# Get-MsolGroupMember

## SYNOPSIS
Retrieves all members of the specified group.

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
The Get-MsolGroupMember cmdlet is used to retrieve members of the specified group.
The members can be either users or groups.

## EXAMPLES

### Example 1: 
```
Get-MsolGroupMember -groupObjectid <id>

          Returns a list of group member objects.
```

Description

-----------

This command retrieves all members (users or groups) of the specified group.

## PARAMETERS

### -All
If present then all results will be returned. 
Cannot be used with MaxResults parameter.

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
The ID of the group to retrieve members for.

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
The maximum number of results returned for a search result.
If not specified, 250 results will be returned.

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
The string to search on.
Only objects with a display name or email address starting with this string will be returned.

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

### -MemberObjectTypes


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
For this cmdlet, each output object will include the following:

            CommonName: The common name of the group.

            DisplayName: The display name of the group.

            EmailAddress: The primary email address of the group (for MailEnabled groups only).

            GroupMemberType: The group type (SecurityGroup, Distributionlist, or MailEnabledSecurityGroup).

            ObjectId: The unique ID of the group.

## NOTES

## RELATED LINKS


