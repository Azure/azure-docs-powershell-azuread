---
external help file: AzureADHelpMSOL.xml
online version: 65f06302-db2d-4507-86b9-752471f47030
schema: 2.0.0
---

# Set-MsolDeviceRegistrationServicePolicy

## SYNOPSIS
Sets the Azure Active Directory device registration service settings.

## SYNTAX

```
Set-MsolDeviceRegistrationServicePolicy [-AllowedToAzureAdJoin] [-AllowedToWorkplaceJoin]
 [-MaximumDevicesPerUser <Int32]>] [-RequireMultiFactorAuth <Boolean]>]
```

## DESCRIPTION
The **Set-MsolDeviceRegistrationServicePolicy** cmdlet sets the Azure Active Directory device registration service settings.

## EXAMPLES

### Example 1: Set the maximum number of devices for a user
```
PS C:\>Set-MsolDeviceRegistratioinServicePolicy -MaximumDevicesPerUser 50
```

This command sets the maximum number of devices a user can have in Azure Active Directory.

### Example 2: Enforce that a user use a second method of authentication
```
PS C:\>Set-MsolDeviceRegistratioinServicePolicy -RequireMultiFactorAuth $True
```

This command enforces users that are adding devices from the internet first use a second method of authentication.

### Example 3: Allow all users to workplace join devices
```
PS C:\>Set-MsolDeviceRegistratioinServicePolicy -AllowedToWorkplaceJoin All
```

This command allows all the users to workplace join devices.

### Example 4: Disallow all users to workplace join devices
```
PS C:\>Set-MsolDeviceRegistratioinServicePolicy -AllowedToWorkplaceJoin None
```

This command disallows any of the users to workplace join devices.

### Example 5: Allow all users to Azure Active Directory join devices
```
PS C:\>Set-MsolDeviceRegistratioinServicePolicy -AllowedToAzureAdJoin All
```

This command allows all the users to Azure Active Directory join devices.

## PARAMETERS

### -AllowedToAzureAdJoin
Specifies what users or group is allowed to join their devices to Azure Active Directory.
When this value is set to All, all users are allowed to Azure Active Directory join devices.
When this value is set to None, no one is allowed to Azure Active Directory join devices.
When this value is set to Selected, only the users and groups from the *AllowedToWorkplaceJoin* parameter Users and Groups are allowed to Azure Active Directory join devices.

The acceptable values for this parameter are:

-- All
-- None
-- Selected

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: All, None, Selected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowedToWorkplaceJoin
Specifies whether user is allowed to join their personal devices to their company.
When set to All, ALL users are allowed to workplace join devices.
When set to None, no one is allowed to workplace join devices.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumDevicesPerUser
Specifies the maximum number of devices a user can have in Azure Active Directory.

```yaml
Type: Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireMultiFactorAuth
Indicates whether users that add devices from the internet must first use a second method of authentication.

```yaml
Type: Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolDeviceRegistrationServicePolicy](65f06302-db2d-4507-86b9-752471f47030)

