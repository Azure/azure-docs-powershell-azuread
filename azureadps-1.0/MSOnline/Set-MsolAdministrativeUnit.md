---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 287EDFB6-E2D4-417A-B8B2-29D6EFD9F1E7
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolAdministrativeUnit

## SYNOPSIS
Updates the properties of an administrative unit.

## SYNTAX

```
Set-MsolAdministrativeUnit [-ObjectId <Guid>] [-DisplayName <String>] [-Description <String>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolAdministrativeUnit** cmdlet updates the properties of an administrative unit.

## EXAMPLES

### Example 1: Modify a description of an administrative unit

```
PS C:\> $AdministrativeUnit = Get-MsolAdministrativeUnit -SearchString "West Coast"
PS C:\> Set-MsolAdministrativeUnit -Description "West Coast region" -ObjectID $AdministrativeUnit.ObjectId
```

The first command gets an administrative unit that matches a search string by using the [Get-MsolAdministrativeUnit](./Get-MsolAdministrativeUnit.md) cmdlet.
The command stores the administrative unit in the $AdministrativeUnit variable.

The second command assigns the description value of West Coast region.
The command specifies the administrative unit by using the object ID of $AdministrativeUnit.

## PARAMETERS

### -ObjectId
Specifies the unique ID of the administrative unit to update.

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

### -DisplayName
Specifies a display name for the administrative unit.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Description
Specifies a description for the administrative unit.

```yaml
Type: String
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

[New-MsolAdministrativeUnit](./New-MsolAdministrativeUnit.md)

[Remove-MsolAdministrativeUnit](./Remove-MsolAdministrativeUnit.md)
