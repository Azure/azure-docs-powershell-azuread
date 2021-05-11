---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
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
The Remove-AzureADMSScopedRoleMembership cmdlet removes a scoped role membership from Azure Active Directory (AD).

## EXAMPLES

### Example 1
```
Remove-AzureADMSScopedRoleMembership -Id "1026185e-25df-4522-a380-7ab697a7241c" -ScopedRoleMembershipId "3028185e-25df-4522-a380-7ab697a7241c"
```

Removes scoped membership.

## PARAMETERS

### -Id
Specifies an object ID.

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

[Add-AzureADMSScopedRoleMembership]()

[Get-AzureADMSScopedRoleMembership]()

