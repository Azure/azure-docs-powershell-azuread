---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: E4C5910F-B006-43F5-8765-E1185A9D0BBE
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolDirSyncFeature

## SYNOPSIS
Sets identity synchronization features for a tenant.

## SYNTAX

```
Set-MsolDirSyncFeature -Feature <String> -Enable <Boolean> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolDirSyncFeature** cmdlet sets identity synchronization features for a tenant.

Synchronization features that can be used with this cmdlet include the following:

- **EnableSoftMatchOnUpn**: Soft match is the process used to link an object being synced from on-premises for the first time with one that already exists in the cloud. When this feature is enabled, soft match will first be attempted using the standard logic, based on the primary SMTP address. If a match is not found based on primary SMTP, then a match will be attempted based on UserPrincipalName. Once this feature is enabled it cannot be disabled.
- **PasswordSync**
- **SynchronizeUpnForManagedUsers**: Allows for the synchronization of UserPrincipalName updates from on-premises for managed (non-federated) users that have been assigned a license. These updates will be blocked if this feature is not enabled. Once this feature is enabled it cannot be disabled.
- **BlockSoftMatch**: When this feature is enabled it will block the soft match feature. Customers are encouraged to enable this feature and keep it at enabled until soft matching is required again for their tenancy. This flag should be enabled again after any soft matching has completed and is no longer needed.
- **BlockCloudObjectTakeoverThroughHardMatch**: When this feature is enabled and an object is synced for which an object with a matching source anchor already exists in Azure AD and that object in Azure AD does not have DirSyncEnabled set to "true", the default behavior would be to hard match the cloud object with the on premises object and set the DirSyncEnabled flag of the Cloud object to "true". <br>
When enabling this feature the cloud object is no longer matched and the DirSyncEnabled flag is not set to "True". Instead, an error is thrown: Error Code: `InvalidHardMatch`, Error Message: `Another cloud created object with the same source anchor already exists in Azure Active Directory`.

Enabling some of these features, such as EnableSoftMatchOnUpn and SynchronizationUpnForManagedUsers, is a permanent operation.
You can't disable these features once they're enabled.

## EXAMPLES

### Example 1: Enable a feature for the tenant
```
PS C:\> Set-MsolDirSyncFeature -Feature EnableSoftMatchOnUpn -Enable $True
```

This command enables the SoftMatchOnUpn feature for the tenant.

### Example 2: Block Soft Matching for the tenant
```
PS C:\> Set-MsolDirSyncFeature -Feature BlockSoftMatch -Enable $True
```

This command enables the BlockSoftMatch feature for the tenant - effectively blocking the Soft Matching feature in the tenant

### Example 3: Block Cloud object takeover through Hard Matching for the tenant
```
PS C:\> Set-MsolDirSyncFeature -Feature BlockCloudObjectTakeoverThroughHardMatch -Enable $True
```

This command enables the BlockCloudObjectTakeoverThroughHardMatch feature for the tenant - effectively blocking the Hard Match object takeover.

## PARAMETERS

### -Feature
Specifies the directory synchronization features to turn on or off.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Enable
Indicates whether the specified feature will be turned on for the company.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant to perform the operation on.
If you do not specify this parameter the cmdlet will use the ID of the current user.
This parameter is only applicable to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolDirSyncFeatures](./Get-MsolDirSyncFeatures.md)
