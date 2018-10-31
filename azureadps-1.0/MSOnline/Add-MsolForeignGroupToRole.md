---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: B5D447B0-4C83-42D7-8162-1E95AF02EDA2
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Add-MsolForeignGroupToRole

## SYNOPSIS
Adds a security group from a partner tenant to a Role in this tenant.

## SYNTAX

```
Add-MsolForeignGroupToRole -ForeignGroupObjectId <Guid> -ForeignCompanyObjectId <Guid> -RoleObjectId <Guid>
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MsolForeignGroupToRole** cmdlet adds a security group from a partner tenant to the specified role in this tenant.

## PARAMETERS

### -ForeignCompanyObjectId
Specifies the object ID of the partner tenant that contains the group to add.

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
Specifies the unique object ID of the group in the partner tenant to add.

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
Specifies the unique object ID of the role to which to add the group.

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
