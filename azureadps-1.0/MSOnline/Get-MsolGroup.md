---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: BFC8C1EC-B14D-45C6-8F11-E128E22C13A8
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolGroup

## SYNOPSIS
Gets groups from Azure Active Directory.

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
The **Get-MsolGroup** cmdlet gets groups from Azure Active Directory.
This cmdlet can be used to return a single group, if you specify the _ObjectId_ parameter, or to search within all groups.

## EXAMPLES

### Example 1: Get a group by using an ID
```
PS C:\> Get-MsolGroup -ObjectId af407072-7ae1-4b07-a0ca-6634b7396054
```

This command returns the group object that has the specified ID.

### Example 2: Get all groups
```
PS C:\> Get-MsolGroup
```

This command returns the entire set of groups for the tenant, up to the default 250 results.

### Example 3: Get a group by using a user principal name
```
PS C:\> Get-MsolGroup -isAgentRole -UserPrincipalName "pattifuller@contoso.com"
```

This command returns the agent groups that a user is a member of.
This only applies for companies that have partner privileges.

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

### -GroupType
Specifies the type of groups to get.
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
Indicates that this cmdlet returns only groups that have validation errors.

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
Specifies that this cmdlet returns only agent groups.
This value applies only to partner users.

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
Specifies the maximum number of results that this cmdlet returns.
The default value is 250.

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
Specifies the unique object ID of the group to get.

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
Specifies a string.
This cmdlet returns security groups that have a display name that start with this string.

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

### -UserObjectId
Specifies the unique ID of a user.
This cmdlet returns security groups to which this user belongs.
This parameter must be used along with the _IsAgentRole_ parameter.

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
Specifies the user principal name of a user.
This cmdlet returns security groups to which this user belongs.
This parameter must be used along with the _IsAgentRole_ parameter.

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
Specifies whether this cmdlet returns only security groups that have license errors.


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
This cmdlet returns a list of groups, which include the following information:

* CommonName. The group's common name.

* Description. A description of the group.

* DisplayName. The group's display name.

* EmailAddress. The group's email addresses.
This is not returned for security groups.

* Errors. A list of errors for the group.

* GroupType. The group's type.
Types can be SecurityGroup, DistributionList or MailEnabledSecurityGroup.

* IsSystem. Whether or not this group is a system group (created by Azure Active Directory).
These groups cannot be updated or removed.

* LastDirSyncTime. The date and time that the group was last synched.

* ManagedBy. The owner of the group.

* ObjectId. The group's unique object ID.

* Proxy Addresses. The proxy addresses associated with this group (for mail-enabled groups only).

* ValidationStatus. Whether or not the group has any errors.

## NOTES

## RELATED LINKS
[New-MsolGroup](./New-MsolGroup.md)

[Remove-MsolGroup](./Remove-MsolGroup.md)

[Set-MsolGroup](./Set-MsolGroup.md)
