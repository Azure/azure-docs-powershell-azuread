---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSPermissionGrantPolicy

## SYNOPSIS
Updates a permission grant policy.

## SYNTAX

```
Set-AzureADMSPermissionGrantPolicy -Id <String> [-Description <String>] [-DisplayName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSPermissionGrantPolicy command updates an Azure Active Directory permission grant policy.

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADMSPermissionGrantPolicy -Id "my_permission_grant_policy_id" -Description "updated description" -DisplayName "update displayname"
```

## PARAMETERS

### -Description
Specifies the description of the permission grant policy.

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
Specifies the display name of the permission grant policy.

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

See the [migration guide for Set-AzureADMSPermissionGrantPolicy](./migrate/Set-AzureADMSPermissionGrantPolicy.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[New-AzureADMSPermissionGrantPolicy](New-AzureADMSPermissionGrantPolicy.md)

[Get-AzureADMSPermissionGrantPolicy](Get-AzureADMSPermissionGrantPolicy.md)

[Remove-AzureADMSPermissionGrantPolicy](Remove-AzureADMSPermissionGrantPolicy.md)

