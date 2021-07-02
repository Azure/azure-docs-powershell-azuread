---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-help.xml
online version:
schema: 2.0.0
ms.assetid: 35904FF0-8D74-4FD7-BB31-44DCAEAFF6BF
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Add-MsolAdministrativeUnitMember

## SYNOPSIS
Adds a member to an administrative unit.

## SYNTAX

```
Add-MsolAdministrativeUnitMember -AdministrativeUnitObjectId <Guid> [-AdministrativeUnitMemberObjectId <Guid>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MsolAdministrativeUnitMember** cmdlet adds a member to an administrative unit.

## EXAMPLES

### Example 1: Add a member to an administrative unit

```
PS C:\> $AdministrativeUnit  = Get-MsolAdministrativeUnit -SearchString "West Coast"
PS C:\> $User = Get-MsolUser -UserPrincipalName "davidchew@contoso.com"
PS C:\> Add-MsolAdministrativeUnitMember -AdministrativeUnitObjectId $AdministrativeUnit.ObjectId -AdministrativeUnitMemberObjectId $User.ObjectId
```

The first command gets an administrative unit that matches a search string by using the [Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md) cmdlet.
The command stores the administrative unit in the $AdministrativeUnit variable.

The second command gets a user for the user principal name davidchew@contoso.com by using the [Get-MsolUser](./Get-MsolUser.md) cmdlet.
The command stores the user in the $User variable.

The final command adds the user in $User to the administrative unit in $AdministrativeUnit.
Both are identified by ObjectId.


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
Specifies the unique object ID of the member to add to the administrative unit.

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
[Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md)

[Get-MsolAdministrativeUnitMember](./Get-MsolAdministrativeUnitMember.md)

[Get-MsolUser](./Get-MsolUser.md)

[Remove-MsolAdministrativeUnitMember](./Remove-MsolAdministrativeUnitMember.md)
