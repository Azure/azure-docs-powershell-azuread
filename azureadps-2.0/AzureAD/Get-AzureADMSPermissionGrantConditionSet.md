---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSPermissionGrantConditionSet

## SYNOPSIS
Get an Azure Active Directory permission grant condition set by id.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPermissionGrantConditionSet -PolicyId <String> -ConditionSetType <String> [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPermissionGrantConditionSet -PolicyId <String> -ConditionSetType <String> -Id <String>
 [<CommonParameters>]
```

## DESCRIPTION
Get an Azure Active Directory permission grant condition set object by id.

## EXAMPLES

### Example 1: Get all permission grant condition sets that are included in the permission grant policy
```
PS C:\>Get-AzureADMSPermissionGrantConditionSet -PolicyId "policy1" -ConditionSetType "includes"
```

### Example 2: Get all permission grant condition sets that are excluded in the permission grant policy
```
PS C:\>Get-AzureADMSPermissionGrantConditionSet -PolicyId "policy1" -ConditionSetType "excludes"
```

### Example 3: Get a permission grant condition set
```
PS C:\>Get-AzureADMSPermissionGrantConditionSet -PolicyId "policy1" -ConditionSetType "includes" -Id "6b5e999b-0ba8-4186-a106-e0296c1c4358"
```

## PARAMETERS

### -PolicyId
The unique identifier of an Azure Active Directory permission grant policy object.

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

### -ConditionSetType
The value indicates whether the condition sets are included in the policy or excluded.

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

### -Id
The unique identifier of an Azure Active Directory permission grant condition set object.

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

## NOTES

See the [migration guide for Get-AzureADMSPermissionGrantConditionSet](./migrate/Get-AzureADMSPermissionGrantConditionSet.md) to the Microsoft Graph PowerShell.

## INPUTS

### string
### string
### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet

## RELATED LINKS

[New-AzureADMSPermissionGrantConditionSet](New-AzureADMSPermissionGrantConditionSet.md)

[Set-AzureADMSPermissionGrantConditionSet](Set-AzureADMSPermissionGrantConditionSet.md)

[Remove-AzureADMSPermissionGrantConditionSet](Remove-AzureADMSPermissionGrantConditionSet.md)
