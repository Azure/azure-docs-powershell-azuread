---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
ms.assetid: 142C8CA5-58AC-4D47-98D5-B3FB7E6A37C7
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Get-AzureADMSScopedRoleMembership

## SYNOPSIS
Gets a scoped role membership from an administrative unit.

## SYNTAX

```
Get-AzureADMSScopedRoleMembership -Id <String> [-ScopedRoleMembershipId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADMSScopedRoleMembership** cmdlet gets a scoped role membership from an administrative unit in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -Id
Specifies the ID of the administrative unit object.


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
Specifies the ID of a scoped role membership.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

[Remove-AzureADMSScopedRoleMembership](./Remove-AzureADMSScopedRoleMembership.md)

