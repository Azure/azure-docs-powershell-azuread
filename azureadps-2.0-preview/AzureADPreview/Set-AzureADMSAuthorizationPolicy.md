---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSAuthorizationPolicy

## SYNOPSIS
Updates an authorization policy.

## SYNTAX

```
Set-AzureADMSAuthorizationPolicy -Id <String> [-BlockMsolPowerShell <Boolean>] [-Description <String>]
 [-DisplayName <String>] [-EnabledPreviewFeatures <System.Collections.Generic.List`1[System.String]>]
 [-GuestUserRoleId <String>]
 [-PermissionGrantPolicyIdsAssignedToDefaultUserRole <System.Collections.Generic.List`1[System.String]>]
 [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSAuthorizationPolicy cmdlet updates an Azure Active Directory authorization policy.

## EXAMPLES

### Example 1: Update an authorization policy
```
PS C:\>Set-AzureADMSAuthorizationPolicy -Id authorizationPolicy -DisplayName "updated displayname" -Description "updated description" -PermissionGrantPolicyIdsAssignedToDefaultUserRole @("user-default-low","application-admin") -GuestUserRoleId "10dae51f-b6af-4016-8d66-8c2a99b929b3" -EnabledPreviewFeatures @("EnableGranularConsent")
```

## PARAMETERS

### -BlockMsolPowerShell
Specifies whether the user-based access to the legacy service endpoint used by MSOL PowerShell is blocked or not.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies the description of the authorization policy.

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
Specifies the display name of the authorization policy.

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

### -EnabledPreviewFeatures
Specifies the preview features enabled for private preview on the tenant.

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

### -GuestUserRoleId
Specifies the roletemplateId for the role that should be granted to guest user.

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
Specifies the unique identifier of the authorization policy.

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

### -PermissionGrantPolicyIdsAssignedToDefaultUserRole
Specifies the policy Ids of permission grant policies assgined to the default user role.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADMSAuthorizationPolicy](Get-AzureADMSAuthorizationPolicy.md)

