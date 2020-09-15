---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
ms.assetid: 937A2A6D-2DF5-43A5-8D2B-8555420254FB
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Remove-AzureADMSScopedRoleMembership

## SYNOPSIS
Removes a scoped role membership.

## SYNTAX

```
Remove-AzureADMSScopedRoleMembership -Id <String> -ScopedRoleMembershipId <String> [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADMSScopedRoleMembership** cmdlet removes a scoped role membership from Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -Id
Specifies the object Id for the administrative unit.

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

### -ScopedRoleMembershipId
Specifies the ID of the scoped role membership to remove.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADMSScopedRoleMembership](./Add-AzureADMSScopedRoleMembership.md)

[Get-AzureADMSScopedRoleMembership](./Get-AzureADMSScopedRoleMembership.md)
