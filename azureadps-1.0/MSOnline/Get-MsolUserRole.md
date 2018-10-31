---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 13C8D948-E093-45E7-A5B5-BC38FAFCCEC7
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolUserRole

## SYNOPSIS
Gets administrator roles to which a user belongs.

## SYNTAX

### ListRolesForUser__0 (Default)
```
Get-MsolUserRole -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### ListRolesForUserByUpn__0
```
Get-MsolUserRole -UserPrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolUserRole** cmdlet gets all of the administrator roles to which the specified user belongs.
This cmdlet will also return roles that the user is a member of through security group membership.

## EXAMPLES

### Example 1: Get user groups
```
PS C:\> Get-MsolUserRole -UserPrincipalName "davidchew@contoso.com"
```
This command retrieves all groups that davidchew@contoso.com is a member of.

## PARAMETERS

### -ObjectId
Specifies the unique ID of the user to retrieve roles for.

```yaml
Type: Guid
Parameter Sets: ListRolesForUser__0
Aliases:

Required: True
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

### -UserPrincipalName
Specifies the user principal name of the user to retrieve roles for.

```yaml
Type: String
Parameter Sets: ListRolesForUserByUpn__0
Aliases:

Required: True
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
