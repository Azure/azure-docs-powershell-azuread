---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 65F06302-DB2D-4507-86B9-752471F47030
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolDeviceRegistrationServicePolicy

## SYNOPSIS
Gets the Azure Active Directory device registration service settings.

## SYNTAX

```
Get-MsolDeviceRegistrationServicePolicy [<CommonParameters>]
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.DeviceRegistrationServicePolicy
This cmdlet returns a **DeviceRegistrationServicePolicy** object, which include the following information: 

- MaximumDevicesPerUser: The maximum number of devices a user can register. 
- RequireMultiFactorAuth: Whether or not users that are adding devices from the internet need to use a second method of authentication. 
- AllowedToWorkplaceJoin: Whether or not users are allowed to workplace join devices. 
- AllowedToAzureAdJoin: Whether or not users are allowed to Azure Active Directory join devices.
If the value is selected, the allowed users are specified in the value of the other two parameters: Groups and Users. 
- Groups: The groups who are allowed to Azure Active Directory join devices. 
- Users: The users who are allowed to Azure Active Directory join devices.

## NOTES

## RELATED LINKS

[Set-MsolDeviceRegistrationServicePolicy](./Set-MsolDeviceRegistrationServicePolicy.md)


