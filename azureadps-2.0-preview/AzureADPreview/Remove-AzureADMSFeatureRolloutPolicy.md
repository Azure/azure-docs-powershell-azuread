---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSFeatureRolloutPolicy

## SYNOPSIS
Allows an admin to remove the policy for cloud authentication roll-out in Azure AD.

## SYNTAX

```
Remove-AzureADMSFeatureRolloutPolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
An admin will use this cmdlet to remove the cloud authentication roll-out policy and have all users where policy applied to be free of the policy.
Users in groups that were assigned to the policy will fall back to the global authentication method (most common case will be federation).

## EXAMPLES

### Example 1: Removes the policy for cloud authentication roll-out in Azure AD.
```
PS C:\> Remove-AzureADMSFeatureRolloutPolicy -Id "7b10cf40-bc0e-46b5-9456-4520179eef5d"
```

This command removes the policy for cloud authentication roll-out in Azure AD.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

[New-AzureADMSFeatureRolloutPolicy](New-AzureADMSFeatureRolloutPolicy.md)

[Get-AzureADMSFeatureRolloutPolicy](Get-AzureADMSFeatureRolloutPolicy.md)

[Set-AzureADMSFeatureRolloutPolicy](Set-AzureADMSFeatureRolloutPolicy.md)

