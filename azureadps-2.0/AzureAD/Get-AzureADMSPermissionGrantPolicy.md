---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSPermissionGrantPolicy

## SYNOPSIS
Gets a permission grant policy.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPermissionGrantPolicy [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPermissionGrantPolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSPermissionGrantPolicy cmdlet gets an Azure Active Directory permission grant policy.

## EXAMPLES

### Example 1: Get a permission grant policy by ID
```
PS C:\> Get-AzureADMSPermissionGrantPolicy -Id "my_permission_grant_policy_id"
```

## PARAMETERS

### -Id
Specifies the unique identifier of the permission grant policy.

```yaml
Type: String
Parameter Sets: GetById
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

[New-AzureADMSPermissionGrantPolicy](New-AzureADMSPermissionGrantPolicy.md)

[Set-AzureADMSPermissionGrantPolicy](Set-AzureADMSPermissionGrantPolicy.md)

[Remove-AzureADMSPermissionGrantPolicy](Remove-AzureADMSPermissionGrantPolicy.md)

