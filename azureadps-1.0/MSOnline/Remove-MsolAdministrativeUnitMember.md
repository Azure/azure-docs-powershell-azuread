---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: DE61C6A6-8503-4FD6-8EDD-C9AAEB62A882
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolAdministrativeUnitMember

## SYNOPSIS
Removes a member from an administrative unit.

## SYNTAX

```
Remove-MsolAdministrativeUnitMember -AdministrativeUnitObjectId <Guid>
 [-AdministrativeUnitMemberObjectId <Guid>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolAdministrativeUnitMember** cmdlet is used to remove a member from an administrative unit.

## EXAMPLES

### Example 1: Remove a member from an administrative unit

```
PS C:\> $AdministrativeUnit = Get-MsolAdministrativeUnit -SearchString "West Coast"
PS C:\> $User = Get-MsolUser -UserPrincipalName "davidchew@contoso.com"
PS C:\> Remove-MsolAdministrativeUnitMember  -AdministrativeUnitObjectId $AdministrativeUnit.ObjectId -AdministrativeUnitMemberObjectId $User.ObjectId
```

The first command gets an administrative unit that matches a search string by using the [Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md) cmdlet.
The command stores the administrative unit in the $AdministrativeUnit variable.

The second command gets a user for the user principal name davidchew@contoso.com by using the [Get-MsolUser](./Get-MsolUser.md) cmdlet.
The command stores the user in the $User variable.

The final command removes the member in $User from the administrative unit in $AdministrativeUnit.

## PARAMETERS

### -AdministrativeUnitObjectId
Specifies the unique object ID of the administrative unit on which this cmdlet operates.

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

### -AdministrativeUnitMemberObjectId
Specifies the unique object ID of the member to remove from the administrative unit.

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
[Add-MsolAdministrativeUnitMember](./Add-MsolAdministrativeUnitMember.md)

[Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md)

[Get-MsolAdministrativeUnitMember](./Get-MsolAdministrativeUnitMember.md)

[Get-MsolUser](./Get-MsolUser.md)
