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
    [- EnabledPrivateFeatures <string>] 
    [- GuestUserRoleId <string>] 
    [- PermissionGrantPolicyIdsAssignedToDefaultUserRole <PermissionGrantPolicyIdList>]
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
