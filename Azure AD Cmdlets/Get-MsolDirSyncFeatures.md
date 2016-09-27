---
external help file: AzureADHelpMSOL.xml
online version: 174960fd-00bb-461f-b8c9-dda519e24f00
schema: 2.0.0
---

# Get-MsolDirSyncFeatures

## SYNOPSIS
Gets the status of identity synchronization features for a tenant.

## SYNTAX

```
Get-MsolDirSyncFeatures [-Feature <String>] [-TenantId <Guid]>]
```

## DESCRIPTION
The **Get-MsolDirSyncProvisioningError** cmdlet gets the status of identity synchronization features for a tenant.

Synchronization features that can be used with this cmdlet include the following:

-- DeviceWriteback
-- DirectoryExtensions
-- DuplicateProxyAddressResiliency
-- DuplicateUPNResiliency
-- EnableSoftMatchOnUpn
-- PasswordSync
-- SynchronizeUpnForManagedUsers
-- UnifiedGroupWriteback
-- UserWriteback

You can run this cmdlet without any feature being specified, in which case it will return a list of all enabled or disabled features.

## EXAMPLES

### Example 1: Get a list of all possible synchronization features
```
PS C:\>Get-MsolDirSyncFeatures
```

This command gets a list of all possible directory synchronization features and whether they are enabled or disabled.

### Example 2: Get a list of all possibleCheck whether the password PasswordSync synchronization features is enabledCheck whether the password is enabled
```
PS C:\>Get-MsolDirSyncFeatures -Feature PasswordSync
```

This command checks whether the password synchronization feature is enabled for the tenant.

## PARAMETERS

### -Feature
Specifies the directory synchronization feature that this cmdlet gets the status of.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
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

[Get-MsolDirSyncConfiguration](174960fd-00bb-461f-b8c9-dda519e24f00)

[Get-MsolDirSyncProvisioningError](ff8b1bba-6ff1-4739-a554-b83079ea4fec)

