---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: C62F46A7-EEE7-41C9-9F71-98C05C11E20D
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Set-AzureADMSAuthorizationPolicy

## SYNOPSIS

## SYNTAX

```
Set-AzureADMSAuthorizationPolicy  
    - Id <string> 
    [- BlockMsolPowerShell <bool>] 
    [- DisplayName <string>] 
    [- Description <string>] 
    [- EnabledPreviewFeatures <System.Collections.Generic.List`1[System.String]>] 
    [- GuestUserRoleId <string>] 
    [- PermissionGrantPolicyIdsAssignedToDefaultUserRole <System.Collections.Generic.List`1[System.String]>]
```

## DESCRIPTION
The **Set-AzureADMSAuthorizationPolicy** cmdlet sets [authorizationPolicy](https://docs.microsoft.com/graph/api/resources/authorizationpolicy?view=graph-rest-beta) object in Azure Active Directory (AD). AuthorizationPolicy is a singleton object, and always exists for the tenant.

## EXAMPLES

### Example 1: Update authorization policy
```
PS C:\>Set-AzureADMSAuthorizationPolicy -Id “authorizationPolicy” -BlockMsolPowerShell $false -DisplayName “new policy name” -Description “new policy description” PermissionGrantPolicyIdsAssignedToDefaultUserRole $PermissionGrantPolicyIdList1
```

## PARAMETERS

### -Id
The Id of the policy for which you want to find the objects

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
### -Description
Specifies a description for the authorization policy.

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
Specifies a display name for the authorization policy.

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
Specifies the roleTemplate Id for the role that should be granted to guest user.

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

### -PermissionGrantPolicyIdsAssignedToDefaultUserRole
Specifies the policy Ids of permission grant policies assigned to the default user role.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
