---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADMSRoleDefinition

## SYNOPSIS
Creates an Azure AD role definition.

## SYNTAX

```
New-AzureADMSRoleDefinition [-Description <String>] -DisplayName <String>
 [-ResourceScopes <System.Collections.Generic.List`1[System.String]>] -IsEnabled <Boolean>
 -RolePermissions <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RolePermission]>
 [-TemplateId <String>] [-Version <String>] [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSRoleDefinition cmdlet creates an Azure Active Directory (Azure AD) role definition.

## EXAMPLES

### Example 1
```powershell
PS C:\>
$allowedResourceAction = @()
$allowedResourceAction += @("microsoft.directory/applications/create")
$rolePermission = @{'allowedResourceActions' = $allowedResourceAction}
$rolePermissions = @()
$rolePermissions += $rolePermission

$resourceScopes = @()
$resourceScopes += '/'

New-AzureADMSRoleDefinition -RolePermissions $rolePermissions -IsEnabled $true -DisplayName 'MyRoleDefinition' -ResourceScopes $resourceScopes

Id              : c466024e-f757-4409-a897-d780916814b1
OdataType       :
Description     :
DisplayName     : fgdf
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
TemplateId      : 4dd5aa9c-cf4d-4895-a993-740d342802b9
Version         :
```

This command creates a new role definition in Azure AD.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnabled
Specifies whether the role definition is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateId
Specifies the template ID for the role definition.

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

## NOTES

See the [migration guide for New-AzureADMSRoleDefinition](./migrate/New-AzureADMSRoleDefinition.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

### Microsoft.Open.MSGraph.Model.DirectoryRoleDefinition

## RELATED LINKS
