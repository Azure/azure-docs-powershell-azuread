---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSPermissionGrantConditionSet

## SYNOPSIS
Delete an Azure Active Directory permission grant condition set by id

## SYNTAX

```
Remove-AzureADMSPermissionGrantConditionSet -PolicyId <String> -ConditionSetType <String> -Id <String>
 [<CommonParameters>]
```

## DESCRIPTION
Delete an Azure Active Directory permission grant condition set object by id.

## EXAMPLES

### Example 1: Delete a permission grant condition set from a policy
```
PS C:\>Remove-AzureADMSPermissionGrantConditionSet -PolicyId "policy1" -ConditionSetType "excludes" -Id "1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5"
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

## NOTES

See the [migration guide for Remove-AzureADMSPermissionGrantConditionSet](./migrate/Remove-AzureADMSPermissionGrantConditionSet.md) to the Microsoft Graph PowerShell.

## INPUTS

### string
### string
### string
## OUTPUTS

## RELATED LINKS

[New-AzureADMSPermissionGrantConditionSet](New-AzureADMSPermissionGrantConditionSet.md)

[Get-AzureADMSPermissionGrantConditionSet](Get-AzureADMSPermissionGrantConditionSet.md)

[Set-AzureADMSPermissionGrantConditionSet](Set-AzureADMSPermissionGrantConditionSet.md)
