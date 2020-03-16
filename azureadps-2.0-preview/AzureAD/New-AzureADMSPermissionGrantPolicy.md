---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSPermissionGrantPolicy

## SYNOPSIS
Creates a permission grant policy.

## SYNTAX

```
New-AzureADMSPermissionGrantPolicy [-Description <String>] [-DisplayName <String>]
 [-Excludes <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet]>]
 [-Includes <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet]>]
 [-Id <String>] [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSPermissionGrantPolicy cmdlet creates an Azure Active Directory permission grant policy.

## EXAMPLES

### Example 1: Create a permission grant policy
```
PS C:\> New-AzureADMSPermissionGrantPolicy -Id "my_new_permission_grant_policy_id"  -DisplayName "MyNewPermissionGrantPolicy" -Description "My new permission grant policy" -Includes @{ PermissionClassification = "low"; PermissionType = "delegated"; Permissions = @{ ResourceApplication = "d4ec8d88-7ea0-4dc5-849b-1a537e9c7956"; IncludeAllPermissions = $false; IncludeSpecificPermissions = @("Device.Read.All","User.Read.All") } }  -Excludes @{ PermissionClassification = "low"; PermissionType = "application"; Permissions = @{ ResourceApplication = "d4ec8d88-7ea0-4dc5-849b-1a537e9c7956"; IncludeAllPermissions = $false; IncludeSpecificPermissions = @("Device.Read.All","User.Read.All") } }
```

## PARAMETERS

### -Description
Specifies the description for the permission grant policy.

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
Specifies the display name for the permission grant policy.

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

### -Excludes
Specifies the conditions to scope what permission scopes should be excluded in the permission grant policy.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the unique identifier of the permission grant policy.

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

### -Includes
Specifies the conditions to scope what permission scopes should be included in the permission grant policy.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet]
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

[Get-AzureADMSPermissionGrantPolicy]()

[Set-AzureADMSPermissionGrantPolicy]()

[Remove-AzureADMSPermissionGrantPolicy]()

