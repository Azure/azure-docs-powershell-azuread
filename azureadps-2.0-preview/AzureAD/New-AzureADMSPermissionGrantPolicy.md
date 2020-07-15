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
New-AzureADMSPermissionGrantPolicy [-Description <String>] [-DisplayName <String>] [-Id <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSPermissionGrantPolicy cmdlet creates an Azure Active Directory permission grant policy.

## EXAMPLES

### Example 1: Create a permission grant policy
```
PS C:\> New-AzureADMSPermissionGrantPolicy -Id "my_new_permission_grant_policy_id"  -DisplayName "MyNewPermissionGrantPolicy" -Description "My new permission grant policy"
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADMSPermissionGrantPolicy]()

[Set-AzureADMSPermissionGrantPolicy]()

[Remove-AzureADMSPermissionGrantPolicy]()

