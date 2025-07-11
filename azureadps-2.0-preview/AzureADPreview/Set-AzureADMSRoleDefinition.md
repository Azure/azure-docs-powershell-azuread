---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSRoleDefinition

## SYNOPSIS
Update a role definition.

## SYNTAX

```
Set-AzureADMSRoleDefinition -Id <String> [-Description <String>] [-DisplayName <String>]
 [-ResourceScopes <System.Collections.Generic.List`1[System.String]>] [-IsEnabled <Boolean>]
 [-RolePermissions <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RolePermission]>]
 [-TemplateId <String>] [-Version <String>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSRoleDefinition cmdlet sets a role definition in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Set-AzureADMSRoleDefinition -ID f2ef992c-3afb-46b9-b7cf-a126ee74c451 -DisplayName 'UpdatedDisplayName'
```

This command updates the specified role definition in Azure AD.

## PARAMETERS

### -Description
Specifies a description for the role definition.

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

### -DisplayName
Specifies a display name for the role definition.

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

### -Id
Specifies Id for the role definition.

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

### -IsEnabled
Specifies whether the role definition is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceScopes
Specifies the resource scopes for the role definition.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RolePermissions
Specifies permissions for the role definition.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RolePermission]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateId
Specifies template id for the role definition.

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

### -Version
Specifies version for the role definition.

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

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-AzureADMSRoleDefinition](Get-AzureADMSRoleDefinition.md)

[New-AzureADMSRoleDefinition](New-AzureADMSRoleDefinition.md)

[Remove-AzureADMSRoleDefinition](Remove-AzureADMSRoleDefinition.md)
