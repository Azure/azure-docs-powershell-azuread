---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSFeatureRolloutPolicy

## SYNOPSIS
Allows an admin to modify the policy for cloud authentication roll-out in Azure AD.

## SYNTAX

```
Set-AzureADMSFeatureRolloutPolicy -Id <String> [-Feature <FeatureEnum>] [-DisplayName <String>]
 [-Description <String>] [-IsEnabled <Boolean>] [-IsAppliedToOrganization <Boolean>]
 [-AppliesTo <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsDirectoryObject]>]
 [<CommonParameters>]
```

## DESCRIPTION
An admin will use this cmdlet to modify the cloud authentication roll-out policy including whether the method for cloud authentication is Pass-through Authentication or not (Password hash-sync) and whether Seamless SSO is enabled.
Users in groups assigned to the policy will start authenticating via the new authentication method and via Seamless SSO if specified.

## EXAMPLES

### Example 1: Updates the policy for cloud authentication roll-out in Azure AD.
```
PS C:\> Set-AzureADMSFeatureRolloutPolicy -Id "a03b6d9e-6654-46e6-8d0a-8ed83c675ca9" -IsEnabled $true
```

This command updates the policy for cloud authentication roll-out in Azure AD.

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

### -DisplayName
Specifies the display name of the cloud authentication roll-out policy.

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

### -Feature
Specifies a feature assigned to the cloud authentication roll-out policy.

Currently, you can assign PassthroughAuthentication | SeamlessSso | PasswordHashSync.

```yaml
Type: FeatureEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnabled
Specifies the status of cloud authentication roll-out policy.

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
Specifies the description of the cloud authentication roll-out policy.

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

### -AppliesTo
Specifies a list of Azure AD objects that is assigned to the feature.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsDirectoryObject]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAppliedToOrganization
Specifies if the cloud authentication roll-out policy applied to the entire organization.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

[New-AzureADMSFeatureRolloutPolicy]()

[Get-AzureADMSFeatureRolloutPolicy]()

[Remove-AzureADMSFeatureRolloutPolicy]()

