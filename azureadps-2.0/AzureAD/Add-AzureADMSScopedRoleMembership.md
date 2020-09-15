---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
ms.assetid: B505822C-4BAA-4EC5-BB0A-128C093930C6
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Add-AzureADMSScopedRoleMembership

## SYNOPSIS
Adds a scoped role membership to an administrative unit.

## SYNTAX

```
Add-AzureADMSScopedRoleMembership -Id <String>
 [-RoleObjectId <String>] [-RoleMemberInfo <RoleMemberInfo>] [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADMSScopedRoleMembership cmdlet adds a scoped role membership to an administrative unit.

## EXAMPLES

### Example 1
```
$User = Get-AzureADUser -SearchString "The user that will be an admin on this unit"
	$Role = Get-AzureADDirectoryRole | Where-Object -Property DisplayName -EQ -Value "User Account Administrator"
	$Unit = Get-AzureADMSAdministrativeUnit | Where-Object -Property DisplayName -Eq -Value "<The display name of the unit"
	$RoleMember = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo
	$RoleMember.ObjectId = $User.ObjectID
	Add-AzureADMSScopedRoleMembership -Id $unit.ObjectId -RoleObjectId $Role.ObjectId -RoleMemberInfo $RoleMember
```

This cmdlet returns the Scope role membership object:
 

	AdministrativeUnitId                 RoleObjectId
	--------------------------           ------------
	c9ab56cc-e349-4237-856e-cab03157a91e 526b7173-5a6e-49dc-88ec-b677a9093709

## PARAMETERS

### -Id
Specifies the ID of an admininstrative unit.
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -RoleMemberInfo
Specifies a **RoleMemberInfo** object. 


```yaml
Type: RoleMemberInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADMSScopedRoleMembership](./Get-AzureADMSScopedRoleMembership.md)

[Remove-AzureADMSScopedRoleMembership](./Remove-AzureADMSScopedRoleMembership.md)

