---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADMSPermissionGrantConditionSet

## SYNOPSIS
Create a new Azure Active Directory permission grant condition set in a given policy.

## SYNTAX

```
New-AzureADMSPermissionGrantConditionSet -PolicyId <String> -ConditionSetType <String>
 [-PermissionType <String>] [-PermissionClassification <String>] [-ResourceApplication <String>]
 [-Permissions <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationTenantIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationPublisherIds <System.Collections.Generic.List`1[System.String]>]
 [-ClientApplicationsFromVerifiedPublisherOnly <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
Create a new Azure Active Directory permission grant condition set object in an existing policy.

## EXAMPLES

### Example 1: Create a basic permission grant condition set in an existing policy with all build in values
```
New-AzureADMSPermissionGrantConditionSet -PolicyId "test1" -ConditionSetType "includes" -PermissionType "delegated"

				Id                                          : cab65448-9ec4-43a5-b575-d1f4d32fefa5
				PermissionType                              : delegated
				PermissionClassification                    : all
				ResourceApplication                         : any
				Permissions                                 : {all}
				ClientApplicationIds                        : {all}
				ClientApplicationTenantIds                  : {all}
				ClientApplicationPublisherIds               : {all}
				ClientApplicationsFromVerifiedPublisherOnly : False
```

### Example 2: Create a permission grant condition set in an existing policy that includes specific permissions for a resource application
```
New-AzureADMSPermissionGrantConditionSet -PolicyId "test1" -ConditionSetType "includes" -PermissionType "delegated" -Permissions @("1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5", "2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6", "3cccccc3-4dd4-5ee5-6ff6-7aaaaaaaaaa7") -ResourceApplication "4dddddd4-5ee5-6ff6-7aa7-8bbbbbbbbbb8"

				Id                                          : 64032dc4-8423-4fd7-930c-a9ed3bb1dbb4
				PermissionType                              : delegated
				PermissionClassification                    : all
				ResourceApplication                         : 4dddddd4-5ee5-6ff6-7aa7-8bbbbbbbbbb8
				Permissions                                 : {1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5, 2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6, 
															  3cccccc3-4dd4-5ee5-6ff6-7aaaaaaaaaa7}
				ClientApplicationIds                        : {all}
				ClientApplicationTenantIds                  : {all}
				ClientApplicationPublisherIds               : {all}
				ClientApplicationsFromVerifiedPublisherOnly : False
```

### Example 3: Create a permission grant condition set in an existing policy that is excluded
```
New-AzureADMSPermissionGrantConditionSet -PolicyId "test1" -ConditionSetType "excludes" -PermissionType "delegated" -Permissions @("1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5", "2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6", "3cccccc3-4dd4-5ee5-6ff6-7aaaaaaaaaa7") -ResourceApplication "4dddddd4-5ee5-6ff6-7aa7-8bbbbbbbbbb8" -PermissionClassification "low" -ClientApplicationsFromVerifiedPublisherOnly $true -ClientApplicationIds @("5eeeeee5-6ff6-7aa7-8bb8-9cccccccccc9", "6ffffff6-7aa7-8bb8-9cc9-0dddddddddd0") -ClientApplicationTenantIds @("7aaaaaa7-8bb8-9cc9-0dd0-1eeeeeeeeee1", "1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5", "2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6") -ClientApplicationPublisherIds @("verifiedpublishermpnid")

			Id                                          : 0f81cce0-a766-4db6-a7e2-4e5f10f6abf8
			PermissionType                              : delegated
			PermissionClassification                    : low
			ResourceApplication                         : 4dddddd4-5ee5-6ff6-7aa7-8bbbbbbbbbb8
			Permissions                                 : {1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5, 2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6, 
														  3cccccc3-4dd4-5ee5-6ff6-7aaaaaaaaaa7}
			ClientApplicationIds                        : {5eeeeee5-6ff6-7aa7-8bb8-9cccccccccc9, 6ffffff6-7aa7-8bb8-9cc9-0dddddddddd0}
			ClientApplicationTenantIds                  : {7aaaaaa7-8bb8-9cc9-0dd0-1eeeeeeeeee1, 1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5, 2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6}
			ClientApplicationPublisherIds               : {verifiedpublishermpnid}
			ClientApplicationsFromVerifiedPublisherOnly : True
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

>[!NOTE]
>There is a hard limit of 100 Application IDs that can be added per tenant.

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

See the [migration guide for New-AzureADMSPermissionGrantConditionSet](./migrate/New-AzureADMSPermissionGrantConditionSet.md) to the Microsoft Graph PowerShell.

## INPUTS

### string
### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.PermissionGrantConditionSet
## NOTES

## RELATED LINKS

[Set-AzureADMSPermissionGrantConditionSet](Set-AzureADMSPermissionGrantConditionSet.md)

[Get-AzureADMSPermissionGrantConditionSet](Get-AzureADMSPermissionGrantConditionSet.md)

[Remove-AzureADMSPermissionGrantConditionSet](Remove-AzureADMSPermissionGrantConditionSet.md)
