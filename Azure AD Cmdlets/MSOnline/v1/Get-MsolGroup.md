---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: BFC8C1EC-B14D-45C6-8F11-E128E22C13A8
---

# Get-MsolGroup

## SYNOPSIS
Retrieves a group from Microsoft Azure Active Directory.

## SYNTAX

### ListGroups__0 (Default)
```
Get-MsolGroup [-UserObjectId <Guid>] [-IsAgentRole] [-UserPrincipalName <String>] [-GroupType <GroupType>]
 [-HasErrorsOnly] [-HasLicenseErrorsOnly <Boolean>] [-SearchString <String>] [-MaxResults <Int32>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### GetGroup__0
```
Get-MsolGroup -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolGroup [-UserObjectId <Guid>] [-IsAgentRole] [-UserPrincipalName <String>] [-GroupType <GroupType>]
 [-HasErrorsOnly] [-HasLicenseErrorsOnly <Boolean>] [-SearchString <String>] [-All] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolGroup cmdlet is used to retrieve groups from Microsoft Azure Active Directory.
This cmdlet can be used to return a single group (if ObjectId is passed in), or to search within all groups.

## EXAMPLES

### Example 1: 
```
Get-MsolGroup -ObjectId <guid>

          None
```

Description

-----------

This command returns the group object with the corresponding ID.

### Example 2: 
```
Get-MsolGroup

          None
```

Description

-----------

This command returns the entire set of groups for the tenant (up to 250).

### Example 3: 
```
Get-MsolGroup -isAgentRole -UserPrincipalName user@contoso.com

          None
```

Description

-----------

This command returns the agent groups that a user is a member of. 
This only applies for companies that have partner privileges.

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

### -GroupType
The filter to return only groups of the specified type.
Valid values are Security, MailEnabledSecurity, and DistributionList.

```yaml
Type: GroupType
Parameter Sets: ListGroups__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HasErrorsOnly
The filter for only groups with validation errors.

```yaml
Type: SwitchParameter
Parameter Sets: ListGroups__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAgentRole
The filter for only agent groups.
Used by partners only.

```yaml
Type: SwitchParameter
Parameter Sets: ListGroups__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
The maximum number of results returned for a search.
If not specified, 250 results will be returned.

```yaml
Type: Int32
Parameter Sets: ListGroups__0
Aliases: 

Required: False
Position: Named
Default value: 250
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
The unique ID of the group to retrieve.

```yaml
Type: Guid
Parameter Sets: GetGroup__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
The string to search on.
Only groups with a display name or email address starting with this string will be returned.

```yaml
Type: String
Parameter Sets: ListGroups__0, All__0
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

### -UserObjectId
The unique ID of a user.
If provided, only groups that this user belongs to will be returned.
This parameter must be used along with IsAgentRole.

```yaml
Type: Guid
Parameter Sets: ListGroups__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
The user ID of a user.
If provided, only groups that this user belongs to will be returned.
This must be used along with IsAgentRole.

```yaml
Type: String
Parameter Sets: ListGroups__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HasLicenseErrorsOnly


```yaml
Type: Boolean
Parameter Sets: ListGroups__0, All__0
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

### Microsoft.Online.Administration.Group
This cmdlet, returns a list of groups, which include the following information:

            CommonName: The group's common name.

            Description: A description of the group.

            DisplayName: The group's display name.

            EmailAddress: The group's email addresses.
This is not returned for security groups.

            Errors: A list of errors for the group.

            GroupType: The group's type.
Types can be SecurityGroup, DistributionList or MailEnabledSecurityGroup.

            IsSystem: Whether or not this group is a system group (created by Microsoft Azure Active Directory). 
These groups cannot be updated or removed.

            LastDirSyncTime: The date and time that the group was last synched.

            ManagedBy: The owner of the group.

            ObjectId: The group's unique object ID.

            Proxy Addresses - the proxy addresses associated with this group (for mail-enabled groups only).

            ValidationStatus: Whether or not the group has any errors.

## NOTES

## RELATED LINKS


