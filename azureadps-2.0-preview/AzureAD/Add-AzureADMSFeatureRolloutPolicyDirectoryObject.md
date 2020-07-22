---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMSFeatureRolloutPolicyDirectoryObject

## SYNOPSIS
Allows an admin to add a group to the cloud authentication roll-out policy in Azure AD.
Users in this group will start authenticating to the cloud per policy.

## SYNTAX

```
Add-AzureADMSFeatureRolloutPolicyDirectoryObject -Id <String> -RefObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
An admin will use this cmdlet to add a group to the cloud authentication roll-out policy.
Users in these groups will start authenticating against the cloud per policy (e.g.
with Seamless Single Sign-On or not, or whether Passthrough auth or not).

## EXAMPLES

### Example 1: Adds a group to the cloud authentication roll-out policy in Azure AD.
```
PS C:\> Add-AzureADMSFeatureRolloutPolicyDirectoryObject -Id "a03b6d9e-6654-46e6-8d0a-8ed83c675ca9" -RefObjectId "0a1068c0-dbb6-4537-9db3-b48f3e31dd76"
```

This command adds a group to the cloud authentication roll-out policy in Azure AD.

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

### -RefObjectId
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

[Remove-AzureADMSFeatureRolloutPolicyDirectoryObject]()

