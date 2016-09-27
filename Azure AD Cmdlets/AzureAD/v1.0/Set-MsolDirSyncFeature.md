---
external help file: AzureADHelpMSOL.xml
online version: f2ed75f9-4313-418d-8b3a-eed1de39b9db
schema: 2.0.0
---

# Set-MsolDirSyncFeature

## SYNOPSIS
Sets identity synchronization features for a tenant.

## SYNTAX

```
Set-MsolDirSyncFeature [-Force] [-TenantId <Guid]>] [-Enable] -Feature <String>
```

## DESCRIPTION
The **Set-MsolDirSyncFeature** cmdlet sets identity synchronization features for a tenant.

Synchronization features that can be used with this cmdlet include the following:

-- DuplicateProxyAddressResiliency. Normally if an object was attempted to be provisioned with a non-unique ProxyAddress, the object would fail to be created/updated due to the uniqueness violation. When this feature is enabled the conflicting ProxyAddress value will be "quarantined" and the object will be provisioned without that specific ProxyAddress value.
-- DuplicateUPNResiliency. Normally if a user attempted to be provisioned with a non-unique UserPrincipalName, the user would fail to be created/updated due to the uniqueness violation. When this feature is enabled the conflicting UPN value will be "quarantined" a temporary UPN will be generated, and the user will be provisioned with that temporary UPN. This UPN will have the format of "\<UserName\>+\<Random Integer\>@\<Tenant Initial Domain\>.onmicrosoft.com".
-- EnableSoftMatchOnUpn. Soft Match is the process used to link an object being synced from on-premises for the first time with one that already exists in the cloud. When this feature is enabled Soft Match will first be attempted using the standard logic, based on primary SMTP address. If a match is not found based on primary SMTP, then a match will be attempted based on UserPrincipalName. Once this feature is enabled it cannot be disabled.
-- PasswordSync
-- SynchronizeUpnForManagedUsers. allows for the synchronization of UserPrincipalName updates from on-premises for managed (non-federated) users that have been assigned a license. These updates will be blocked if this feature is not enabled. Once this feature is enabled it cannot be disabled.

Enabling some of these features, such as EnableSoftMatchOnUpn and SynchronizationUpnForManagedUsers is a permanent operation.
These features cannot be disabled once they are enabled.

## EXAMPLES

### Example 1: Enable a feature for the tenant
```
PS C:\>Set-MsolDirSyncFeature -Feature EnableSoftMatchOnUpn -Enable $True
```

This command enables the SoftMatchOnUpn feature for the tenant.

## PARAMETERS

### -Enable
Indicates whether the specified feature will be turned on for the company.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -Feature
Specifies the directory synchronization features to turn on or off.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant to perform the operation on.
If you do not specify this parameter the cmdlet will use the ID of the current user.
This parameter is only applicable to partner users.

```yaml
Type: Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolDirSyncFeatures](f2ed75f9-4313-418d-8b3a-eed1de39b9db)

