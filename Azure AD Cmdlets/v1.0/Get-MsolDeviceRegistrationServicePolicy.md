---
external help file: AzureADHelpMSOL.xml
online version: 3df291fc-2a4e-4493-8c1e-bfe2977b5f15
schema: 2.0.0
---

# Get-MsolDeviceRegistrationServicePolicy

## SYNOPSIS
Gets the Azure Active Directory device registration service settings.

## SYNTAX

```
Get-MsolDeviceRegistrationServicePolicy
```

## DESCRIPTION
The **Get-MsolDeviceRegistrationServicePolicy** cmdlet gets the Azure Active Directory device registration service settings.

## EXAMPLES

### Example 1: Get the Azure Active Directory device registration service policy settings
```
PS C:\>Get-MsolDeviceRegistrationServicePolicy
```

This command gets the Azure Active Directory device registration service policy settings.

## PARAMETERS

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.DeviceRegistrationServicePolicy
This cmdlet returns a **DeviceRegistrationServicePolicy** object, which include the following information: 

-- MaximumDevicesPerUser: The maximum number of devices a user can register. 
-- RequireMultiFactorAuth: Whether or not users that are adding devices from the internet need to use a second method of authentication. 
-- AllowedToWorkplaceJoin: Whether or not users are allowed to workplace join devices. 
-- AllowedToAzureAdJoin: Whether or not users are allowed to Azure Active Directory join devices.
If the value is selected, the allowed users are specified in the value of the other two parameters: Groups and Users. 
-- Groups: The groups who are allowed to Azure Active Directory join devices. 
-- Users: The users who are allowed to Azure Active Directory join devices.

## NOTES

## RELATED LINKS

[Set-MsolDeviceRegistrationServicePolicy](3df291fc-2a4e-4493-8c1e-bfe2977b5f15)

