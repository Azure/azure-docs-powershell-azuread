---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSRoleAssignment

## SYNOPSIS
Creates an Azure AD role assignment.

## SYNTAX

```
New-AzureADMSRoleAssignment -RoleDefinitionId <String> -PrincipalId <String> -ResourceScope <String>
 [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSRoleAssignment cmdlet creates an Azure Active Directory (Azure AD) role assignment.

## EXAMPLES

### Example 1
```powershell
PS C:\> New-AzureADMSRoleAssignment -RoleDefinitionId 62e90356-69f5-4237-9190-012177145e10 -PrincipalId 69584089-b4d1-4055-9c94-320412efd653 -ResourceScope '/'
```

This command creates a new role assignment.

## PARAMETERS

### -PrincipalId
Specifies the principal for role assignment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceScope
Specifies the resource scope for role assignment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
Specifies the role definition for role assignment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
[Get-AzureADMSRoleAssignment]()

[Remove-AzureADMSRoleAssignment]()