---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSFeatureRolloutPolicy

## SYNOPSIS
Allows an admin to create the policy for cloud authentication roll-out in Azure AD.

## SYNTAX

```
New-AzureADMSFeatureRolloutPolicy -Feature <FeatureEnum> -DisplayName <String> [-Description <String>]
 -IsEnabled <Boolean> [-IsAppliedToOrganization <Boolean>]
 [-AppliesTo <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsDirectoryObject]>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to create the policy for cloud authentication roll-out (users moving from federation to cloud auth) in Azure AD.
The policy admin can identify whether the users will authenticate using password hashes in Azure AD (Password hash-sync) or Active Directory on-premises directly (Pass-through authentication).

## EXAMPLES

### Example 1: Creates the policy for cloud authentication roll-out in Azure AD.
```
PS C:\> New-AzureADMSFeatureRolloutPolicy -Feature PassthroughAuthentication -DisplayName "Passthrough Authentication Rollout Policy" -IsEnabled $true

          Feature                 : PassthroughAuthentication
          Id                      : 7ca3e599-e8cc-4d31-9ed6-19dd4f88e833
          DisplayName             : Passthrough Authentication Rollout Policy
          Description             :
          IsEnabled               : True
          IsAppliedToOrganization : False
          AppliesTo               :
```

This command creates the policy for cloud authentication roll-out in Azure AD.

## PARAMETERS

### -DisplayName
Specifies the display name of the cloud authentication roll-out policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

Required: True
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

Required: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.MsFeatureRolloutPolicy
## NOTES
## RELATED LINKS

[Get-AzureADMSFeatureRolloutPolicy]()

[Set-AzureADMSFeatureRolloutPolicy]()

[Remove-AzureADMSFeatureRolloutPolicy]()

