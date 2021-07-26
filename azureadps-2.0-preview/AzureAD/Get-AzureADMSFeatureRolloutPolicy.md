---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSFeatureRolloutPolicy

## SYNOPSIS
Gets the policy for cloud authentication roll-out in Azure Active Directory.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSFeatureRolloutPolicy [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADMSFeatureRolloutPolicy [-SearchString <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSFeatureRolloutPolicy -Id <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to get the policy for cloud authentication rollout (users moving from federation to cloud auth) in Azure AD.
This policy is in the form of one or two FeatureRolloutPolicy objects holding groups that are assigned for cloud auth (Pass-through auth or Password hash-sync) and groups that are assigned for Seamless Single Sign-On (feature on top of PTA or PHS).

## EXAMPLES

### Example 1: Retrieves a list of all cloud authentication roll-out in Azure AD.
```
PS C:\> Get-AzureADMSFeatureRolloutPolicy

          Feature                 : PassthroughAuthentication
          Id                      : 7ca3e599-e8cc-4d31-9ed6-19dd4f88e833
          DisplayName             : Passthrough Authentication Rollout Policy
          Description             :
          IsEnabled               : True
          IsAppliedToOrganization : False
          AppliesTo               :
```

This command retrieves a list of all cloud authentication roll-out policies in Azure AD.

### Example 2: Retrieves cloud authentication roll-out in Azure AD with given Id.
```
PS C:\> Get-AzureADMSFeatureRolloutPolicy -Id "a03b6d9e-6654-46e6-8d0a-8ed83c675ca9"

          Feature                 : PassthroughAuthentication
          Id                      : a03b6d9e-6654-46e6-8d0a-8ed83c675ca9
          DisplayName             : Passthrough Authentication Rollout Policy
          Description             :
          IsEnabled               : True
          IsAppliedToOrganization : False
          AppliesTo               :
```

This command retrieves the policy for cloud authentication roll-out policy in Azure AD.

### Example 3: Retrieves cloud authentication roll-out in Azure AD with given Search String.
```
PS C:\> Get-AzureADMSFeatureRolloutPolicy -SearchString "Default PasswordHashSync Rollout Policy"

          Feature                 : PasswordHashSync
          Id                      : a03b6d9e-6654-46e6-8d0a-8ed83c675ca9
          DisplayName             : Default PasswordHashSync Rollout Policy
          Description             : Default PasswordHashSync Rollout Policy
          IsEnabled               : True
          IsAppliedToOrganization : False
          AppliesTo               :
```

This command retrieves the policy for cloud authentication roll-out policy in Azure AD.

## PARAMETERS

### -Id
The unique identifier of the cloud authentication roll-out policy in Azure AD.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
The oData v3.0 filter statement. 
Controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.MsFeatureRolloutPolicy
## NOTES
## RELATED LINKS

[New-AzureADMSFeatureRolloutPolicy]()

[Set-AzureADMSFeatureRolloutPolicy]()

[Remove-AzureADMSFeatureRolloutPolicy]()

