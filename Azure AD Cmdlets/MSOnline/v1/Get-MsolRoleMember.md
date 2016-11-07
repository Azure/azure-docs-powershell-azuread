---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: C38ED8D1-68B3-4D78-8386-20F6FC87A167
---

# Get-MsolRoleMember

## SYNOPSIS
Retrieves all members of the specified role.

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
The Get-MsolRoleMember cmdlet is used to retrieve all members of the specified role.

## EXAMPLES

### Example 1: 
```
$role = Get-MsolRole -RoleName "Company Administrator"
          Get-MsolRoleMember -RoleObjectId $role.ObjectId

          Returns a list of role member objects.
```

Description

-----------

This command returns all the members of the specified role.

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

### -MaxResults
The maximum number of results returned for a search result.
If not specified, 250 results will be returned.

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
The ID of the role to retrieve members for.

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

### Microsoft.Online.Administation.RoleMember
For this cmdlet, each RoleMember object will include the following:

            DisplayName: The display name of the role member.

            EmailAddress: The email address of the role member.

            IsLicensed: Whether or not the user is licensed.

            LastDirSyncTime: The date and time that this member was last synced.

            ObjectId: The unique ID of the member.

            OverallProvisioningStatus: The provisioning status of this user.

            RoleMemberType; The type of role member.
Currently only "User" is supported.

            ValidationStatus: Whether or not there are any errors with this group member.

## NOTES

## RELATED LINKS


