---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSFeatureRolloutPolicyDirectoryObject

## SYNOPSIS
Allows an admin to remove a group from the cloud authentication rollout policy in Azure AD.
Users in this group will revert back to the authenticating using the global policy (in most cases this will be federation).

## SYNTAX

```
Remove-AzureADMSFeatureRolloutPolicyDirectoryObject -Id <String> -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
An admin will use this cmdlet to remove groups from the cloud authentication roll-out policy.
Users in these groups will start authenticating against the global authentication policy (e.g.
federation).

## EXAMPLES

### Example 1: Removes a group from the cloud authentication roll-out policy from Azure AD.
```
PS C:\> Remove-AzureADMSFeatureRolloutPolicyDirectoryObject -Id "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -ObjectId "bbbbbbbb-1111-2222-3333-cccccccccccc"
```

This command removes a group from the cloud authentication roll-out policy from Azure AD.

## PARAMETERS

### -Id
The unique identifier of the cloud authentication roll-out policy in Azure AD.

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

### -ObjectId
The unique identifier of the specific Azure AD object that will be assigned to the cloud authentication roll-out policy in Azure AD.

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
## RELATED LINKS

[Add-AzureADMSFeatureRolloutPolicyDirectoryObject](Add-AzureADMSFeatureRolloutPolicyDirectoryObject.md)
