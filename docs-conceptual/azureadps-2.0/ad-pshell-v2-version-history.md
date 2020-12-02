---
title: 'Azure Active Directory PowerShell for Graph: Version release history | Microsoft Docs'
description: This article lists all releases of the AzureAD and AzureADPreview PowerShell modules
services: active-directory
documentationcenter: ''
author: billmath
manager: daveba
editor: ''
ms.service: active-directory
ms.devlang: na
ms.topic: reference
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 06/24/2019
ms.subservice: hybrid
ms.author: billmath
ms.collection: M365-identity-device-management
---
# Azure Active Directory PowerShell for Graph: Version release history
The Azure Active Directory (Azure AD) team regularly updates Azure AD Connect with new features and functionality. The Azure Active Directory PowerShell for Graph modules are available in a General Availability version (AzureAD module) and a preview version (AzureADPreview module). This document contains the release history of both modules.

This article is designed to help you keep track of the versions that have been released, and to understand what the changes are in the latest version.

## 2.0.2.85 - Preview release of the AzureADPreview module

### Release status 

02/25/2020: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.85)

### New features and improvements 

The following new cmdlets were added to the AzureADPreview module:

- Support for AuthorizationPolicy and PermissionGrantPolicy API
  - Get-AzureADMSAuthorizationPolicy
  - Set-AzureADMSAuthorizationPolicy
  - Get-AzureADMSPermissionGrantPolicy
  - New-AzureADMSPermissionGrantPolicy
  - Remove-AzureADMSPermissionGrantPolicy
- Add label assignment capability to New-AzureADMSGroup and Set-AzureADMSGroup
- Add ResetRedemption parameter to New-AzureADMSInvitation to reset an external user's invitation redemption

## 2.0.2.77 - Preview release of the AzureADPreview module

### Release status 

11/22//2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.77)

### New features and improvements 

The following new cmdlets were added to the AzureADPreview module:

- `Get-AzureADMSApplication`
- `New-AzureADMSApplication`
- `Set-AzureADMSApplication`
- `Set-AzureADMSApplicationLogo`
- `Remove-AzureADMSApplication`
- `New-AzureADMSApplicationPassword`
- `Remove-AzureADMSApplicationPassword`
- `New-AzureADMSApplicationKey`
- `Remove-AzureADMSApplicationKey`
- `Get-AzureADMSApplicationOwner`
- `Add-AzureADMSApplicationOwner`
- `Remove-AzureADMSApplicationOwner`
- `Get-AzureADMSApplicationExtensionProperty`
- `New-AzureADMSApplicationExtensionProperty`
- `Remove-AzureADMSApplicationExtensionProperty`

The new **Get-AzureADMSApplication** cmdlet retrieves the list of applications within the organization.

The new **New-AzureADMSApplication** cmdlet creates (registers) a new application object.

The new **Set-AzureADMSApplication** cmdlet updates the properties of an application object.

The new **Set-AzureADMSApplicationLogo** cmdlet sets the logo for an application object.

The new **Remove-AzureADMSApplication** cmdlet deletes an application object.

The new **New-AzureADMSApplicationPassword** cmdlet adds a strong password to an application.

The new **Remove-AzureADMSApplicationPassword** cmdlet remove a password from an application.

The new **New-AzureADMSApplicationKey** cmdlet adds a new key to an application.

The new **Remove-AzureADMSApplicationKey** cmdlet removes a key from an application.

The new **Get-AzureADMSApplicationOwner** cmdlet retrieves the list of owners for an application object.

The new **Add-AzureADMSApplicationOwner** cmdlet adds an owner for an application object.

The new **Remove-AzureADMSApplicationOwner** cmdlet removes an owner from an application object.

The new **Get-AzureADMSApplicationExtensionProperty** cmdlet retrieves the list of extension properties on an application object.

The new **New-AzureADMSApplicationExtensionProperty** cmdlet creates an extension property on an application object.

The new **Remove-AzureADMSApplicationExtensionProperty** cmdlet deletes an extension property from an application object.

All the things you can do in the existing cmdlets can also be done through the new "MS" version of cmdlets. Applications created using the new **New-AzureADMSApplication** cmdlet can sign-in Work/School, Personal Microsoft Account users.


## 2.0.2.76 - General Availability release of the AzureAD module

### Release status 

11/22//2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.76)

### New features and improvements 

The following new cmdlets were added to the AzureAD module:

- `Get-AzureADMSApplication`
- `New-AzureADMSApplication`
- `Set-AzureADMSApplication`
- `Set-AzureADMSApplicationLogo`
- `Remove-AzureADMSApplication`
- `New-AzureADMSApplicationPassword`
- `Remove-AzureADMSApplicationPassword`
- `New-AzureADMSApplicationKey`
- `Remove-AzureADMSApplicationKey`
- `Get-AzureADMSApplicationOwner`
- `Add-AzureADMSApplicationOwner`
- `Remove-AzureADMSApplicationOwner`
- `Get-AzureADMSApplicationExtensionProperty`
- `New-AzureADMSApplicationExtensionProperty`
- `Remove-AzureADMSApplicationExtensionProperty`

The new **Get-AzureADMSApplication** cmdlet retrieves the list of applications within the organization.

The new **New-AzureADMSApplication** cmdlet creates (registers) a new application object.

The new **Set-AzureADMSApplication** cmdlet updates the properties of an application object.

The new **Set-AzureADMSApplicationLogo** cmdlet sets the logo for an application object.

The new **Remove-AzureADMSApplication** cmdlet deletes an application object.

The new **New-AzureADMSApplicationPassword** cmdlet adds a strong password to an application.

The new **Remove-AzureADMSApplicationPassword** cmdlet remove a password from an application.

The new **New-AzureADMSApplicationKey** cmdlet adds a new key to an application.

The new **Remove-AzureADMSApplicationKey** cmdlet removes a key from an application.

The new **Get-AzureADMSApplicationOwner** cmdlet retrieves the list of owners for an application object.

The new **Add-AzureADMSApplicationOwner** cmdlet adds an owner for an application object.

The new **Remove-AzureADMSApplicationOwner** cmdlet removes an owner from an application object.

The new **Get-AzureADMSApplicationExtensionProperty** cmdlet retrieves the list of extension properties on an application object.

The new **New-AzureADMSApplicationExtensionProperty** cmdlet creates an extension property on an application object.

The new **Remove-AzureADMSApplicationExtensionProperty** cmdlet deletes an extension property from an application object.

All the things you can do in the existing cmdlets can also be done through the new "MS" version of cmdlets. Applications created using the new **New-AzureADMSApplication** cmdlet can sign-in Work/School, Personal Microsoft Account users.

## 2.0.2.62 - Public preview release of the AzureADPreview module

### Release status 

11/13/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.62)

### New features and improvements

The following new cmdlets are added in this release:

 - Add-AzureADMSServicePrincipalDelegatedPermissionClassification
 - Get-AzureADMSApplicationTemplate
 - Get-AzureADMSPasswordSingleSignOnCredential
 - Get-AzureADMSServicePrincipalDelegatedPermissionClassification
 - New-AzureADMSPasswordSingleSignOnCredential
 - Remove-AzureADMSPasswordSingleSignOnCredential
 - Remove-AzureADMSServicePrincipalDelegatedPermissionClassification
 - Set-AzureADMSPasswordSingleSignOnCredential

The new **-AzureADMSServicePrincipalDelegatedPermissionClassification** cmdlets enable customers to create/read and delete delegated permission classifications which are contained entity defined on the Azure Active Directory ServicePrincipal entity.

The new **-AzureADMSPasswordSingleSignOnCredential** cmdlets allow customers to manage the credentials for Password SSO applications. Users can perform operation to their own credentials, users can read group credentials, and application owner or global admin with the right roles and RBAC permission can do CRUD operations for other user or group credentials. 

The new **Get-AzureADMSApplicationTemplate** allows customers to list the applicationTemplate objects from the AzureAD Gallery / App Marketplace.

We added support for **-IsAssignableToRole** parameter in both **Get-AzureADMSGroup** and **New-AzureADMSGroup** cmdlets.  Groups with this property set can only be created by principals with designated permissions.
 
### Fixed issues 
This release fixes a bug where the **Set-AzureADTrustedCertificateAuthority** cmdlet, in specific conditions, was unable to properly set CrlDistributionPoint.

## 2.0.2.61 - General availability release of the AzureAD module

### Release status 

11/13/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.61)

### Fixed issues 
This release fixes a bug where the **Set-AzureADDomain** and **New-AzureADDomain** cmdlets would not allow the user to properly set the IsDefaultForCloudRedirections property.

## 2.0.2.53 - Public preview release of the AzureADPreview module

### Release status 

10/10/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.53)

### New features and improvements

Added support for -IsDefaultForCloudRedirection parameter in New-AzureADDomain and Set-AzureADDomain cmdlets
 
### Fixed issues 
This release fixes a bug where the Set-AzureADTrustedCertificateAuthority cmdlet, in specific conditions, was unable to properly set CrlDistributionPoint.

## 2.0.2.52 - General availability release of the AzureAD module

### Release status 

10/10/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.52)

### New features and improvements

Added support for -IsDefaultForCloudRedirection parameter in New-AzureADDomain and Set-AzureADDomain cmdlets

### Fixed issues 
This release fixes a bug where the Set-AzureADTrustedCertificateAuthority cmdlet, in specific conditions, was unable to properly set CrlDistributionPoint.

## 2.0.2.51 - Public preview release of the AzureADPreview module

### Release status 

09/20/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.51)

### Fixed issues 
This release fixes a bug where the Disconnect-AzureAD cmdlet, in specific conditions, did not clear a cached token in the PowerShell session.


## 2.0.2.50 - General availability release of the AzureAD module

### Release status 

09/20/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.50)

### Fixed issues 
This release fixes a bug where the Disconnect-AzureAD cmdlet, in specific conditions, did not clear a cached token in the PowerShell session.

## 2.0.2.39 - Preview release of the AzureAD Preview module


### Release status 

09/09/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.39)

### New features and improvements

The following new cmdlets are added in this release:

 - Add-AzureADMSFeatureRolloutPolicyDirectoryObject
 - Get-AzureADMSFeatureRolloutPolicy
 - New-AzureADMSFeatureRolloutPolicy
 - Remove-AzureADMSFeatureRolloutPolicy
 - Remove-AzureADMSFeatureRolloutPolicyDirectoryObject
 - Set-AzureADMSFeatureRolloutPolicy

## 2.0.2.32 - Preview release of the AzureADPreview module

### Release status 

08/02/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.32)

### New features and improvements 
The following new cmdlets are added in this release:

 - Get-AzureADMSRoleAssignment

 - Get-AzureADMSRoleDefinition

 - New-AzureADMSRoleAssignment

 - New-AzureADMSRoleDefinition

 - Remove-AzureADMSRoleAssignment

 - Remove-AzureADMSRoleDefinition

 - Set-AzureADMSRoleDefinition

Added support for -Filter parameter in Get-AzureADDirectoryRole cmdlet

## 2.0.2.31 - General Availability release of the AzureAD module

### Release status 

08/02/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.31)

### New features and improvements 
Added support for -Filter parameter in Get-AzureADDirectoryRole cmdlet

## 2.0.2.25 - General Availability release of the AzureAD module

### Release status 

06/21/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/2.0.2.25)

### New features and improvements 
- Support for setting CompanyName property through `Set-AzureADUser` cmdlet. Example:  `Set-AzureADUser -ObjectId <> -CompanyName <>`


### Fixed issues 

- Fix for bug  - `Get-AzureADUser` -searchstring fails with error " Message: Unsupported or invalid query filter clause specified for property 'userState' of resource 'User'."
- Fix for bug  - `Get-AzureADUserOwnedObject` fails with error  “The given key was not present in the dictionary”

## 2.0.2.24 - Preview release of the AzureADPreview module

### Release status 

06/21//2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.24)

### New features and improvements 

The following new cmdlets were added to the AzureADPreview module:

#### Privileged Role Management

- `Add-AzureADMSPrivilegedResource`
- `Close-AzureADMSPrivilegedRoleAssignmentRequest`
- `Get-AzureADMSPrivilegedResource`
- `Get-AzureADMSPrivilegedRoleAssignment`
- `Get-AzureADMSPrivilegedRoleAssignmentRequest`
- `Get-AzureADMSPrivilegedRoleDefinition`
- `Get-AzureADMSPrivilegedRoleSetting`
- `Open-AzureADMSPrivilegedRoleAssignmentRequest`
- `Set-AzureADMSPrivilegedRoleAssignmentRequest`
- `Set-AzureADMSPrivilegedRoleSetting`

Read more about [Azure AD Privileged Role management](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/)

#### Trust Framework Policy Management

- `New-AzureADMSTrustFrameworkPolicy`
- `Get-AzureADMSTrustFrameworkPolicy`
- `Remove-AzureADMSTrustFrameworkPolicy`
- `Set-AzureADMSTrustFrameworkPolicy`

Read more about the [B2C Trust Framework policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-trustframeworks-defined-ief-custom#understand-trust-framework-policies)

#### Directory Auditing

- `Get-AzureADAuditDirectoryLogs`
- `Get-AzureADAuditSignInLogs`

Read more about [Azure AD directory auditing](https://docs.microsoft.com/azure/active-directory/reports-monitoring/)

## 2.0.2.17 Public Preview release of the AzureADPreview module
### Release status
4/9/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.17)

## 2.0.2.16 General Availability release of the AzureAD module
### Release status
4/9/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.2.16)

## 2.0.2.15 Public Preview release of the AzureADPreview module
### Release status
4/6/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.15)

## 2.0.2.14 General Availability  release of the AzureAD module
### Release status
4/6/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.2.14)

## 2.0.2.5 Public Preview release of the AzureADPreview module
### Release status
10/5/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.5)

## 2.0.2.4 General Availability release of the AzureAD module
### Release status
10/5/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.2.4)

## 2.0.2.3 Public Preview release of the AzureADPreview module
### Release status
10/3/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.2.3)

## 2.0.2.2 General Availability release of the AzureAD module
### Release status
10/3/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.2.2)

## 2.0.1.18 Public Preview release of the AzureADPreview module
### Release status
6/28/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.1.18)

## 2.0.1.17 Public Preview release of the AzureADPreview module
### Release status
6/21/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.1.17)

## 2.0.1.16 General Availability release of the AzureAD module
### Release status
6/21/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.1.16)

## 2.0.1.11 Public Preview release of the AzureADPreview module
### Release status
5/7/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.1.11)

## 2.0.1.10 General Availability release of the AzureAD module
### Release status
5/7/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.1.10)

## 2.0.1.9 Public Preview release of the AzureADPreview module
### Release status
5/2/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.1.9)

## 2.0.1.6 General Availability of the AzureAD module
### Release status
5/2/2019: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.1.6)

## 2.0.1.3 General Availability release of the AzureAD module
### Release status
3/20/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.1.3)

## 2.0.1.2 Public Preview release of the AzureADPreview module
### Release status
3/19/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.1.2)

## 2.0.0.155 General Availability release of the AzureAD module
### Release status
2/15/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.155)

## 2.0.0.154 Public Preview release of the AzureADPreview module
### Release status
2/14/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.154)

## 2.0.0.150 Public Preview release of the AzureADPreview module
### Release status
2/14/2018: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.150)

## 2.0.0.137 Public Preview release of the AzureADPreview module
### Release status
8/6/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.137)

## 2.0.0.131 General Availability release of the AzureAD module
### Release status
7/10/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.131)

## 2.0.0.129 Public Preview release of the AzureADPreview module
### Release status
7/10/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.129)

## 2.0.0.127 Public Preview release of the AzureADPreview module
### Release status
6/8/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.127)

## 2.0.0.125 Public Preview release of the AzureADPreview module
### Release status
6/8/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.125)

## 2.0.0.115 General Availability release of the AzureAD module
### Release status
5/1/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.115)

## 2.0.0.114 Public Preview release of the AzureADPreview module
### Release status
5/1/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.114)

## 2.0.0.110 Public Preview release of the AzureADPreview module
### Release status
4/18/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.110)

## 2.0.0.109 General Availability release of the AzureAD module
### Release status
4/17/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.109)

## 2.0.0.98 Public Preview release of the AzureADPreview module
### Release status
3/28/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.98)

## 2.0.0.98 General Availability release of the AzureAD module
### Release status
3/28/2017 : Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.98)

## 2.0.0.85 Public Preview release of the AzureADPreview module
### Release status
3/17/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.85)

## 2.0.0.76 Public Preview release of the AzureADPreview module
### Release status
3/7/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.76)

## 2.0.0.71 General Availability release of the AzureAD module
### Release status
3/1/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.71)

## 2.0.0.55 General Availability release of the AzureAD module
### Release status
2/9/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.55)

## 2.0.0.52 Public Preview release of the AzureADPreview module
### Release status
1/25/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.52)

## 2.0.0.50 Public Preview release of the AzureADPreview module
### Release status
1/11/2017: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.50)

## 2.0.0.44 Public Preview release of the AzureADPreview module
### Release status
12/7/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.44)

## 2.0.0.40 Public Preview release of the AzureADPreview module
### Release status
12/2/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.40)

## 2.0.0.39 Public Preview release of the AzureADPreview module
### Release status
12/1/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.39)

## 2.0.0.38 Public Preview release of the AzureADPreview module
### Release status
11/30/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.38)

## 2.0.0.33 Public Preview release of the AzureADPreview module
### Release status
11/21/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.33)

## 2.0.0.33 General Availability release of the AzureAD module
### Release status
11/21/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.33)

## 2.0.0.30 General Availability release of the AzureAD module
### Release status
11/17/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD /2.0.0.30)

## 2.0.0.2 Public Preview release of the AzureADPreview module
### Release status
9/22/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.2)

## 2.0.0.17 Public Preview release of the AzureADPreview module
### Release status
10/25/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.17)

## 2.0.0.7 Public Preview release of the AzureADPreview module
### Release status
10/6/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.7)

## 2.0.0.1 Public Preview release of the AzureADPreview module
### Release status
9/12/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/2.0.0.1)

## 1.1.167.0 Public Preview release of the AzureADPreview module
### Release status
8/12/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/1.1.167.0)

## 1.1.159.0 Public Preview release of the AzureADPreview module
### Release status
8/3/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/1.1.159.0)

## 1.1.147.0 Public Preview release of the AzureADPreview module
### Release status
7/8/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/1.1.147.0)

## 1.1.146.0 Public Preview release of the AzureADPreview module
### Release status
7/7/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/1.1.146.0)

## 1.1.143.0 Public Preview release of the AzureADPreview module
### Release status
6/30/2016: Released for installation and upgrade from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureADPreview/1.1.143.0)
