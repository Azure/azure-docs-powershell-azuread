---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSPermissionGrantConditionSet

## SYNOPSIS
Update an existing Azure Active Directory permission grant condition set.

## SYNTAX

```
Set-AzureADMSPermissionGrantConditionSet -PolicyId <String> -ConditionSetType <String> -Id <String>
 [-PermissionType <String>] [-PermissionClassification <String>] [-ResourceApplication <String>]
 [-Permissions <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationTenantIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationPublisherIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationsFromVerifiedPublisherOnly <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Updates an Azure Active Directory permission grant condition set object identified by id.

## EXAMPLES

### Example 1: Update a permission grant condition set to includes permissions that has been classified as low.
```
1. Get existing permission grant policy by that need to be updated.
		
		$permissionGrantConditionSet =Get-AzureADMSPermissionGrantConditionSet -PolicyId "test1" -ConditionSetType "includes" -Id "1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5"

			Id                                          : 1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5
			PermissionType                              : delegated
			PermissionClassification                    : all
			ResourceApplication                         : ec8d61c9-1cb2-4edb-afb0-bcda85645555
			Permissions                                 : {8b590330-0eb2-45d0-baca-a00ecf7e7b87, dac1c8fa-e6e4-47b8-a128-599660b8cd5c, 
														  f6db0cc3-88cd-4c74-a374-3d8c7cc4c50b}
			ClientApplicationIds                        : {4a6c40ea-edc1-4202-8620-dd4060ee6583, 17a961bd-e743-4e6f-8097-d7e6612999a7}
			ClientApplicationTenantIds                  : {17a961bd-e743-4e6f-8097-d7e6612999a8, 17a961bd-e743-4e6f-8097-d7e6612999a9, 
														  17a961bd-e743-4e6f-8097-d7e6612999a0}
			ClientApplicationPublisherIds               : {verifiedpublishermpnid}
			ClientApplicationsFromVerifiedPublisherOnly : True
			
		2. Update PermissionClassification 
		
		Set-AzureADMSPermissionGrantConditionSet -PolicyId "test1" -ConditionSetType "includes" -Id $permissionGrantConditionSet.Id -PermissionClassification low

			Id                                          : 1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5
			PermissionType                              : delegated
			PermissionClassification                    : low
			ResourceApplication                         : ec8d61c9-1cb2-4edb-afb0-bcda85645555
			Permissions                                 : {8b590330-0eb2-45d0-baca-a00ecf7e7b87, dac1c8fa-e6e4-47b8-a128-599660b8cd5c, 
														  f6db0cc3-88cd-4c74-a374-3d8c7cc4c50b}
			ClientApplicationIds                        : {4a6c40ea-edc1-4202-8620-dd4060ee6583, 17a961bd-e743-4e6f-8097-d7e6612999a7}
			ClientApplicationTenantIds                  : {17a961bd-e743-4e6f-8097-d7e6612999a8, 17a961bd-e743-4e6f-8097-d7e6612999a9, 
														  17a961bd-e743-4e6f-8097-d7e6612999a0}
			ClientApplicationPublisherIds               : {verifiedpublishermpnid}
			ClientApplicationsFromVerifiedPublisherOnly : True
```

### Example 2: Update a permission grant condition set
```
PS C:\>Set-AzureADMSPermissionGrantConditionSet -PolicyId "policy1" -ConditionSetType "includes" -Id "2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6" -PermissionType "Delegated" -PermissionClassification "Low" -ResourceApplication "3cccccc3-4dd4-5ee5-6ff6-7aaaaaaaaaa7" -Permissions @("4dddddd4-5ee5-6ff6-7aa7-8bbbbbbbbbb8") -ClientApplicationIds @("All") -ClientApplicationTenantIds @("All") -ClientApplicationPublisherIds @("All") -ClientApplicationsFromVerifiedPublisherOnly $true
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

### -PermissionType
Specific type of permissions (application, delegated) to scope consent operation down to.

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

### -PermissionClassification
Specific classification (all, low, medium, high) to scope consent operation down to.

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

### -Permissions
The identifier of the resource application to scope consent operation down to.
It could be @("All") or a list of permission ids.

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

### -ClientApplicationIds
The set of client application ids to scope consent operation down to.
It could be @("All") or a list of client application Ids.

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

### -ClientApplicationTenantIds
The set of client application tenant ids to scope consent operation down to.
It could be @("All") or a list of client application tenant ids.

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

### -ClientApplicationPublisherIds
The set of client applications publisher ids to scope consent operation down to.
It could be @("All") or a list of client application publisher ids.

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

### -ClientApplicationsFromVerifiedPublisherOnly
A value indicates whether to only includes client applications from verified publishers.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceApplication
The identifier of the resource application to scope consent operation down to.
It could be "Any" or a specific resource application id.

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

See the [migration guide for Set-AzureADMSPermissionGrantConditionSet](./migrate/Set-AzureADMSPermissionGrantConditionSet.md) to the Microsoft Graph PowerShell.

## INPUTS

### string
### string
### string
## OUTPUTS

## RELATED LINKS

[New-AzureADMSPermissionGrantConditionSet](New-AzureADMSPermissionGrantConditionSet.md)

[Get-AzureADMSPermissionGrantConditionSet](Get-AzureADMSPermissionGrantConditionSet.md)

[Remove-AzureADMSPermissionGrantConditionSet](Remove-AzureADMSPermissionGrantConditionSet.md)
