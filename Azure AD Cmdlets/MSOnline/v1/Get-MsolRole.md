---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 430D359B-200B-4EA6-A6B7-D347A0264CC9
---

# Get-MsolRole

## SYNOPSIS
Retrieves administrator roles.

## SYNTAX

### ListRoles__0 (Default)
```
Get-MsolRole [-TenantId <Guid>] [<CommonParameters>]
```

### GetRole__0
```
Get-MsolRole -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### GetRoleByName__0
```
Get-MsolRole -RoleName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolRole cmdlet can be used to retrieve a list of administrator roles.

## EXAMPLES

### Example 1:
```
PS C:\> Get-MsolRole

          Returns a list of role objects.
```

Description

-----------

This command retrieves administrator roles for the company.

## PARAMETERS

### -ObjectId
The ObjectId of the role to retrieve.

```yaml
Type: Guid
Parameter Sets: GetRole__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleName
The name of the role to retrieve.

```yaml
Type: String
Parameter Sets: GetRoleByName__0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Role
For this cmdlet, each output object will include the following fields:

            Description: A description of the role.

            IsEnabled: Whether or not the role is enabled.

            IsSystem: Whether or not the role was created by Microsoft Azure Active Directory.

            Name: The name of the role.

            ObjectId: The unique ID of the role.

## NOTES

## RELATED LINKS
