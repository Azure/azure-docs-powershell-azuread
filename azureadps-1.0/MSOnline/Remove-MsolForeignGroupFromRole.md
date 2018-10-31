---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 563E6FCE-8B24-4952-A82E-3FA5A7339886
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolForeignGroupFromRole

## SYNOPSIS
Removes a security group from a partner tenant.

## SYNTAX

```
Remove-MsolForeignGroupFromRole -ForeignGroupObjectId <Guid> -ForeignCompanyObjectId <Guid>
 -RoleObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolForeignGroupFromRole** cmdlet removes a security group from a partner tenant for a specified role in this tenant.

## EXAMPLES


## PARAMETERS

### -ForeignCompanyObjectId
Specifies the object ID of the partner tenant that contains the group to remove.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForeignGroupObjectId
Specifies the unique object ID of the group in the partner tenant to remove.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleObjectId
Specifies the unique object ID of the role from which to remove the group.

```yaml
Type: Guid
Parameter Sets: (All)
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

## NOTES

## RELATED LINKS
[Add-MsolForeignGroupToRole](./Add-MsolForeignGroupToRole.md)
