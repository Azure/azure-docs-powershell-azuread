---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMSScopedRoleMembership

## SYNOPSIS
Adds a scoped role membership to an administrative unit.

## SYNTAX

```
Add-AzureADMSScopedRoleMembership -Id <String> [-AdministrativeUnitId <String>] [-RoleId <String>]
 [-RoleMemberInfo <MsRoleMemberInfo>] [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADMSScopedRoleMembership cmdlet adds a scoped role membership to an administrative unit.

## EXAMPLES

### Example 1
```
$User = Get-AzureADUser -SearchString "The user that will be an admin on this unit"
	$Role = Get-AzureADDirectoryRole | Where-Object -Property DisplayName -Eq -Value "User Account Administrator"
	$Unit = Get-AzureADMSAdministrativeUnit | Where-Object -Property DisplayName -Eq -Value "The display name of the unit"
	$RoleMember = New-Object -TypeName Microsoft.Open.MSGraph.Model.MsRolememberinfo.RoleMemberInfo
	$RoleMember.Id = $User.ObjectID
	Add-AzureADMSScopedRoleMembership -Id $Unit.Id -RoleId $Role.ObjectId -RoleMemberInfo $RoleMember
```

This cmdlet returns the Scoped role membership object.

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
Specifies a RoleMemberInfo object.

```yaml
Type: MsRoleMemberInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUnitId
{{ Fill AdministrativeUnitId Description }}

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

### -RoleId
{{ Fill RoleId Description }}

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

[Get-AzureADMSScopedRoleMembership]()

[Remove-AzureADMSScopedRoleMembership]()

