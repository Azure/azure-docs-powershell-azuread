---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: F432C01F-578C-47DE-A3FA-9CCAA42F4814
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolAdministrativeUnitMember

## SYNOPSIS
Gets members of an administrative unit.

## SYNTAX

### ListAdministrativeUnitMembers__0 (Default)
```
Get-MsolAdministrativeUnitMember [-AdministrativeUnitObjectId <Guid>] [-MaxResults <Int32>] [-TenantId <Guid>]
 [<CommonParameters>]
```

### All__0
```
Get-MsolAdministrativeUnitMember [-AdministrativeUnitObjectId <Guid>] [-All] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolAdministrativeUnitMember** cmdlet gets members of an administrative unit.

## EXAMPLES

### Example 1: Get members of an administrative unit

```
PS C:\> $AdministrativeUnit = Get-MsolAdministrativeUnit -SearchString "West Coast"
PS C:\> Get-MsolAdministrativeUnitMember -AdministrativeUnitObjectId $AdminstrativeUnit.ObjectId
```

The first command gets an administrative unit that matches a search string by using the [Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md) cmdlet.
The command stores the administrative unit in the $AdministrativeUnit variable.

The second command returns all members of the administrative unit in $AdministrativeUnit.

## PARAMETERS

### -AdministrativeUnitObjectId
Specifies the unique object ID of the administrative unit on which this cmdlet operates.

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
Specifies the maximum number of results that this cmdlet returns.

```yaml
Type: Int32
Parameter Sets: ListAdministrativeUnitMembers__0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.AdministrativeUnitMember
This this cmdlet returns objects that contain the following:

* DisplayName. The display name of the administrative unit member.
* EmailAddress. The user principal name of the administrative unit member.
* ObjectId. The unique ID of the administrative unit member.

## NOTES

## RELATED LINKS
[Add-MsolAdministrativeUnitMember](./Add-MsolAdministrativeUnitMember.md)

[Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md)

[Remove-MsolAdministrativeUnitMember](./Remove-MsolAdministrativeUnitMember.md)
