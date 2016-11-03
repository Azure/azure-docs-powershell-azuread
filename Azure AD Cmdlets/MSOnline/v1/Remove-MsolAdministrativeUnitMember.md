---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: DE61C6A6-8503-4FD6-8EDD-C9AAEB62A882
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
The Remove-MsolAdministrativeUnitMember cmdlet is used to remove a member from an administrative unit.

## EXAMPLES

### --------------------------  Example 1  --------------------------
@{paragraph=PS C:\\\>}



```
$au = Get-MsolAdministrativeUnit -searchstring "West Coast"
          $user = Get-MsolUser -UserPrincipalName "user@contoso.com"
          Remove-MsolAdministrativeUnitMember  -AdministrativeUnitObjectId $au.ObjectId -AdministrativeUnitMemberObjectId $user.ObjectId
```

Description

-----------

This command removes member user@contoso.com from the administrative unit "West Coast".

## PARAMETERS

### -AdministrativeUnitObjectId
AdministrativeUnitMemberObjectId

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
The ID of the administrative unit to remove members from.

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
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


