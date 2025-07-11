---
Module Name: AzureAD
Module Guid: b433e830-b479-4f7f-9c80-9cc6c28e1b51
Locale: en-US
ms.assetid: 7D9D9507-ADE5-45BD-97F8-0CCCDA3D3B58
ms.reviewer: stevemutungi
ms.custom: iamfeature=PowerShell
---

# AzureAD Module

## Description

>[!IMPORTANT]
> Azure AD and MSOnline PowerShell modules are deprecated as of March 30, 2024. To learn more, read the [deprecation update](https://techcommunity.microsoft.com/t5/microsoft-entra-blog/important-update-deprecation-of-azure-ad-powershell-and-msonline/ba-p/4094536)). After this date, support for these modules are limited to migration assistance to Microsoft Graph PowerShell SDK and security fixes. The deprecated modules will continue to function through March, 30 2025.
>
> We recommend migrating to [Microsoft Graph PowerShell](/powershell/microsoftgraph/overview) to interact with Microsoft Entra ID (formerly Azure AD). For common migration questions, refer to the [Migration FAQ](/powershell/azure/active-directory/migration-faq). *Note:* Versions 1.0.x of MSOnline may experience disruption after June 30, 2024.

The Azure Active Directory PowerShell for Graph module can be downloaded and installed from the [PowerShell Gallery](https://www.powershellgallery.com/packages/AzureAD/). The gallery uses the PowerShellGet module. The PowerShellGet module requires PowerShell 3.0 or newer and requires one of the following operating systems:

- Windows 10
- Windows 8.1 Pro
- Windows 8.1 Enterprise
- Windows 7 SP1
- Windows Server 2016 TP5
- Windows Server 2012 R2
- Windows Server 2008 R2 SP1

PowerShellGet also requires .NET Framework 4.5 or above. You can install .NET Framework 4.5 or above from [here](https://www.microsoft.com/en-us/download/details.aspx?id=30653).

For more detailed info on installation of the AzureAD cmdlets please see: [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/en-us/powershell/azure/active-directory/install-adv2).

These are the cmdlets in the Azure Active Directory PowerShell for Graph module.

## AzureAD Cmdlets

### [Add-AzureADApplicationOwner](Add-AzureADApplicationOwner.md)
Adds an owner to an application.

### [Add-AzureADDeviceRegisteredOwner](Add-AzureADDeviceRegisteredOwner.md)
Adds a registered owner for a device.

### [Add-AzureADDeviceRegisteredUser](Add-AzureADDeviceRegisteredUser.md)
Adds a registered user for a device.

### [Add-AzureADDirectoryRoleMember](Add-AzureADDirectoryRoleMember.md)
Adds a member to a directory role.

### [Add-AzureADGroupMember](Add-AzureADGroupMember.md)
Adds a member to a group.

### [Add-AzureADGroupOwner](Add-AzureADGroupOwner.md)
Adds an owner to a group.

### [Add-AzureADMSAdministrativeUnitMember](Add-AzureADMSAdministrativeUnitMember.md)
Adds an administrative unit member.

### [Add-AzureADMSApplicationOwner](Add-AzureADMSApplicationOwner.md)
Adds an owner for an application object.

### [Add-AzureADMSLifecyclePolicyGroup](Add-AzureADMSLifecyclePolicyGroup.md)
Adds a group to a lifecycle policy

### [Add-AzureADMSScopedRoleMembership](Add-AzureADMSScopedRoleMembership.md)
Adds a scoped role membership to an administrative unit.

### [Add-AzureADMSServicePrincipalDelegatedPermissionClassification](Add-AzureADMSServicePrincipalDelegatedPermissionClassification.md)
Add a classification for a delegated permission.

### [Add-AzureADServicePrincipalOwner](Add-AzureADServicePrincipalOwner.md)
Adds an owner to a service principal.

### [Confirm-AzureADDomain](Confirm-AzureADDomain.md)
Validate the ownership of a domain.

### [Connect-AzureAD](Connect-AzureAD.md)
Connects with an authenticated account to use Active Directory cmdlet requests.

### [Disconnect-AzureAD](Disconnect-AzureAD.md)
Disconnects the current session from an Azure Active Directory tenant.

### [Enable-AzureADDirectoryRole](Enable-AzureADDirectoryRole.md)
Activates an existing directory role in Azure Active Directory.

### [Get-AzureADApplication](Get-AzureADApplication.md)
Gets an application.

### [Get-AzureADApplicationExtensionProperty](Get-AzureADApplicationExtensionProperty.md)
Gets application extension properties.

### [Get-AzureADApplicationKeyCredential](Get-AzureADApplicationKeyCredential.md)
Gets the key credentials for an application.

### [Get-AzureADApplicationLogo](Get-AzureADApplicationLogo.md)
Retrieve the logo of an application

### [Get-AzureADApplicationOwner](Get-AzureADApplicationOwner.md)
Gets the owner of an application.

### [Get-AzureADApplicationPasswordCredential](Get-AzureADApplicationPasswordCredential.md)
Gets the password credential for an application.

### [Get-AzureADApplicationProxyApplication](Get-AzureADApplicationProxyApplication.md)
The Get-AzureADApplicationProxyApplication cmdlet retrieves an application configured for Application Proxy in Azure Active Directory.

### [Get-AzureADApplicationProxyApplicationConnectorGroup](Get-AzureADApplicationProxyApplicationConnectorGroup.md)
The Get-AzureADApplicationProxyApplicationConnectorGroup cmdlet retrieves the connector group assigned for a specific application.

### [Get-AzureADApplicationProxyConnector](Get-AzureADApplicationProxyConnector.md)
The Get-AzureADApplicationProxyApplicationConnector cmdlet a list of all connectors, or if specified, details of a specific connector.

### [Get-AzureADApplicationProxyConnectorGroup](Get-AzureADApplicationProxyConnectorGroup.md)
The Get-AzureADApplicationProxyConnectorGroup cmdlet retrieves a list of all connector groups, or if specified, details of a specific connector group.

### [Get-AzureADApplicationProxyConnectorGroupMember](Get-AzureADApplicationProxyConnectorGroupMember.md)
{{ Fill in the Synopsis }}

### [Get-AzureADApplicationProxyConnectorGroupMembers](Get-AzureADApplicationProxyConnectorGroupMembers.md)
The Get-AzureADApplicationProxyConnectorGroupMembers gets all the Application Proxy connectors associated with the given connector group.

### [Get-AzureADApplicationProxyConnectorMemberOf](Get-AzureADApplicationProxyConnectorMemberOf.md)
The Get-AzureADApplicationProxyConnectorMemberOf command gets the ConnectorGroup that the specified Connector is a member of.

### [Get-AzureADApplicationServiceEndpoint](Get-AzureADApplicationServiceEndpoint.md)
Retrieve the service endpoint of an application

### [Get-AzureADContact](Get-AzureADContact.md)
Gets a contact from Azure Active Directory.

### [Get-AzureADContactDirectReport](Get-AzureADContactDirectReport.md)
Get the direct reports for a contact.

### [Get-AzureADContactManager](Get-AzureADContactManager.md)
Gets the manager of a contact.

### [Get-AzureADContactMembership](Get-AzureADContactMembership.md)
Get a contact membership.

### [Get-AzureADContactThumbnailPhoto](Get-AzureADContactThumbnailPhoto.md)
Retrieves the thumbnail photo of a contact

### [Get-AzureADContract](Get-AzureADContract.md)
Gets a contract.

### [Get-AzureADCurrentSessionInfo](Get-AzureADCurrentSessionInfo.md)
This cmdlet will return the current session state

### [Get-AzureADDeletedApplication](Get-AzureADDeletedApplication.md)
Retrieves the list of previously deleted applications

### [Get-AzureADDevice](Get-AzureADDevice.md)
Gets a device from Active Directory.

### [Get-AzureADDeviceConfiguration](Get-AzureADDeviceConfiguration.md)
This cmdlet retrieves the device configuration object

### [Get-AzureADDeviceRegisteredOwner](Get-AzureADDeviceRegisteredOwner.md)
Gets the registered owner of a device.

### [Get-AzureADDeviceRegisteredUser](Get-AzureADDeviceRegisteredUser.md)
Gets a registered user.

### [Get-AzureADDirectoryRole](Get-AzureADDirectoryRole.md)
Gets a directory role.

### [Get-AzureADDirectoryRoleMember](Get-AzureADDirectoryRoleMember.md)
Gets members of a directory role.

### [Get-AzureADDirectoryRoleTemplate](Get-AzureADDirectoryRoleTemplate.md)
Gets directory role templates.

### [Get-AzureADDomain](Get-AzureADDomain.md)
Gets a domain.

### [Get-AzureADDomainNameReference](Get-AzureADDomainNameReference.md)
This cmdlet retrieves the objects that are referenced by a given domain name

### [Get-AzureADDomainServiceConfigurationRecord](Get-AzureADDomainServiceConfigurationRecord.md)
Gets the domain's service configuration records from the serviceConfigurationRecords navigation property.

### [Get-AzureADDomainVerificationDnsRecord](Get-AzureADDomainVerificationDnsRecord.md)
Retrieve the domain verification DNS record for a domain

### [Get-AzureADExtensionProperty](Get-AzureADExtensionProperty.md)
Gets  extension properties registered with Azure AD.

### [Get-AzureADGroup](Get-AzureADGroup.md)
Gets a group (via Microsoft Graph).

### [Get-AzureADGroupAppRoleAssignment](Get-AzureADGroupAppRoleAssignment.md)
Gets a group application role assignment.

### [Get-AzureADGroupMember](Get-AzureADGroupMember.md)
Gets a member of a group.

### [Get-AzureADGroupOwner](Get-AzureADGroupOwner.md)
Gets an owner of a group.

### [Get-AzureADMSAdministrativeUnit](Get-AzureADMSAdministrativeUnit.md)
Gets an administrative unit.

### [Get-AzureADMSAdministrativeUnitMember](Get-AzureADMSAdministrativeUnitMember.md)
Gets a member of an administrative unit.

### [Get-AzureADMSApplication](Get-AzureADMSApplication.md)
Retrieves the list of applications within the organization.

### [Get-AzureADMSApplicationExtensionProperty](Get-AzureADMSApplicationExtensionProperty.md)
Retrieves the list of extension properties on an application object.

### [Get-AzureADMSApplicationOwner](Get-AzureADMSApplicationOwner.md)
Retrieves the list of owners for an application object.

### [Get-AzureADMSAuthorizationPolicy](Get-AzureADMSAuthorizationPolicy.md)
Gets an authorization policy, which represents a policy that can control Azure Active Directory authorization settings.

### [Get-AzureADMSConditionalAccessPolicy](Get-AzureADMSConditionalAccessPolicy.md)
Gets an Azure Active Directory conditional access policy.

### [Get-AzureADMSDeletedDirectoryObject](Get-AzureADMSDeletedDirectoryObject.md)
This cmdlet is used to retrieve a soft deleted directory object from the directory

### [Get-AzureADMSDeletedGroup](Get-AzureADMSDeletedGroup.md)
This cmdlet is used to retrieve the soft deleted groups in a directory.

### [Get-AzureADMSGroup](Get-AzureADMSGroup.md)
Gets information about groups in the Microsoft Entra ID (via MS Graph).

### [Get-AzureADMSGroupLifecyclePolicy](Get-AzureADMSGroupLifecyclePolicy.md)
Retrieves the properties and relationships of a groupLifecyclePolicies object in Azure Active Directory. If you specify no parameters, this cmdlet gets all groupLifecyclePolicies.

### [Get-AzureADMSIdentityProvider](Get-AzureADMSIdentityProvider.md)
This cmdlet is used to retrieve the configured identity providers in the directory.

### [Get-AzureADMSLifecyclePolicyGroup](Get-AzureADMSLifecyclePolicyGroup.md)
Retrieves the lifecycle policy object to which a group belongs.

### [Get-AzureADMSNamedLocationPolicy](Get-AzureADMSNamedLocationPolicy.md)
Gets an Azure Active Directory named location policy.

### [Get-AzureADMSPermissionGrantConditionSet](Get-AzureADMSPermissionGrantConditionSet.md)
Get an Azure Active Directory permission grant condition set by id.

### [Get-AzureADMSPermissionGrantPolicy](Get-AzureADMSPermissionGrantPolicy.md)
Gets a permission grant policy.

### [Get-AzureADMSRoleAssignment](Get-AzureADMSRoleAssignment.md)
Gets information about role assignments in Azure AD.

### [Get-AzureADMSRoleDefinition](Get-AzureADMSRoleDefinition.md)
Gets information about role definitions in Azure AD.

### [Get-AzureADMSScopedRoleMembership](Get-AzureADMSScopedRoleMembership.md)
Gets a scoped role membership from an administrative unit.

### [Get-AzureADMSServicePrincipalDelegatedPermissionClassification](Get-AzureADMSServicePrincipalDelegatedPermissionClassification.md)
Retreive the delegated permission classification objects on a service principal.

### [Get-AzureADOAuth2PermissionGrant](Get-AzureADOAuth2PermissionGrant.md)
Gets OAuth2PermissionGrant entities.

### [Get-AzureADObjectByObjectId](Get-AzureADObjectByObjectId.md)
Retrieves the object(s) specified by the objectIds parameter

### [Get-AzureADServiceAppRoleAssignedTo](Get-AzureADServiceAppRoleAssignedTo.md)
Gets app role assignments for this app or service, granted to users, groups and other service principals.

### [Get-AzureADServiceAppRoleAssignment](Get-AzureADServiceAppRoleAssignment.md)
Gets a service principal application role assignment.

### [Get-AzureADServicePrincipal](Get-AzureADServicePrincipal.md)
Gets a service principal.

### [Get-AzureADServicePrincipalCreatedObject](Get-AzureADServicePrincipalCreatedObject.md)
Get objects created by a service principal.

### [Get-AzureADServicePrincipalKeyCredential](Get-AzureADServicePrincipalKeyCredential.md)
Get key credentials for a service principal.

### [Get-AzureADServicePrincipalMembership](Get-AzureADServicePrincipalMembership.md)
Get a service principal membership.

### [Get-AzureADServicePrincipalOAuth2PermissionGrant](Get-AzureADServicePrincipalOAuth2PermissionGrant.md)
Gets an oAuth2PermissionGrant object.

### [Get-AzureADServicePrincipalOwnedObject](Get-AzureADServicePrincipalOwnedObject.md)
Gets an object owned by a service principal.

### [Get-AzureADServicePrincipalOwner](Get-AzureADServicePrincipalOwner.md)
Get the owner of a service principal.

### [Get-AzureADServicePrincipalPasswordCredential](Get-AzureADServicePrincipalPasswordCredential.md)
Get credentials for a service principal.

### [Get-AzureADSubscribedSku](Get-AzureADSubscribedSku.md)
Gets subscribed SKUs to Microsoft services.

### [Get-AzureADTenantDetail](Get-AzureADTenantDetail.md)
Gets the details of a tenant.

### [Get-AzureADTrustedCertificateAuthority](Get-AzureADTrustedCertificateAuthority.md)
Gets the trusted certificate authority.

### [Get-AzureADUser](Get-AzureADUser.md)
Gets a user.

### [Get-AzureADUserAppRoleAssignment](Get-AzureADUserAppRoleAssignment.md)
Get a user application role assignment.

### [Get-AzureADUserCreatedObject](Get-AzureADUserCreatedObject.md)
Get objects created by the user.

### [Get-AzureADUserDirectReport](Get-AzureADUserDirectReport.md)
Get the user's direct reports.

### [Get-AzureADUserExtension](Get-AzureADUserExtension.md)
Gets a user extension.

### [Get-AzureADUserLicenseDetail](Get-AzureADUserLicenseDetail.md)
Retrieves license details for a user

### [Get-AzureADUserManager](Get-AzureADUserManager.md)
Gets the manager of a user.

### [Get-AzureADUserMembership](Get-AzureADUserMembership.md)
Get user memberships.

### [Get-AzureADUserOAuth2PermissionGrant](Get-AzureADUserOAuth2PermissionGrant.md)
Gets an oAuth2PermissionGrant object.

### [Get-AzureADUserOwnedDevice](Get-AzureADUserOwnedDevice.md)
Get registered devices owned by a user.

### [Get-AzureADUserOwnedObject](Get-AzureADUserOwnedObject.md)
Get objects owned by a user.

### [Get-AzureADUserRegisteredDevice](Get-AzureADUserRegisteredDevice.md)
Get devices registered by a user.

### [Get-AzureADUserThumbnailPhoto](Get-AzureADUserThumbnailPhoto.md)
Retrieve the thumbnail photo of a user

### [Get-CrossCloudVerificationCode](Get-CrossCloudVerificationCode.md)
Gets the verification code used to validate the ownership of the domain in another connected cloud. Important: Only applies to a verified domain.

### [New-AzureADApplication](New-AzureADApplication.md)
Creates an application.

### [New-AzureADApplicationExtensionProperty](New-AzureADApplicationExtensionProperty.md)
Creates an application extension property.

### [New-AzureADApplicationKeyCredential](New-AzureADApplicationKeyCredential.md)
Creates a key credential for an application.

### [New-AzureADApplicationPasswordCredential](New-AzureADApplicationPasswordCredential.md)
Creates a password credential for an application.

### [New-AzureADApplicationProxyApplication](New-AzureADApplicationProxyApplication.md)
The New-AzureADApplicationProxyApplication cmdlet creates a new application configured for Application Proxy in Azure Active Directory.

### [New-AzureADApplicationProxyConnectorGroup](New-AzureADApplicationProxyConnectorGroup.md)
The New-AzureADApplicationProxyConnectorGroup cmdlet creates a new Application Proxy Connector group.

### [New-AzureADDevice](New-AzureADDevice.md)
Creates a device.

### [New-AzureADDomain](New-AzureADDomain.md)
Creates a domain.

### [New-AzureADGroup](New-AzureADGroup.md)
Creates a group.

### [New-AzureADGroupAppRoleAssignment](New-AzureADGroupAppRoleAssignment.md)
Assign a group of users to an application role.

### [New-AzureADMSAdministrativeUnit](New-AzureADMSAdministrativeUnit.md)
Creates an administrative unit.

### [New-AzureADMSApplication](New-AzureADMSApplication.md)
Creates (registers) a new application object.

### [New-AzureADMSApplicationExtensionProperty](New-AzureADMSApplicationExtensionProperty.md)
Creates an extension property on an application object.

### [New-AzureADMSApplicationKey](New-AzureADMSApplicationKey.md)
Adds a new key to an application.

### [New-AzureADMSApplicationPassword](New-AzureADMSApplicationPassword.md)
Adds a strong password to an application.

### [New-AzureADMSConditionalAccessPolicy](New-AzureADMSConditionalAccessPolicy.md)
Creates a new conditional access policy in Azure Active Directory.

### [New-AzureADMSGroup](New-AzureADMSGroup.md)
Creates an Azure AD group.

### [New-AzureADMSGroupLifecyclePolicy](New-AzureADMSGroupLifecyclePolicy.md)
Creates a new groupLifecyclePolicy

### [New-AzureADMSIdentityProvider](New-AzureADMSIdentityProvider.md)
This cmdlet is used to configure a new identity provider in the directory.

### [New-AzureADMSInvitation](New-AzureADMSInvitation.md)
This cmdlet is used to invite a new external user to your directory.

### [New-AzureADMSNamedLocationPolicy](New-AzureADMSNamedLocationPolicy.md)
Creates a new named location policy in Azure Active Directory.

### [New-AzureADMSPermissionGrantConditionSet](New-AzureADMSPermissionGrantConditionSet.md)
Create a new Azure Active Directory permission grant condition set in a given policy.

### [New-AzureADMSPermissionGrantPolicy](New-AzureADMSPermissionGrantPolicy.md)
Creates a permission grant policy.

### [New-AzureADMSRoleAssignment](New-AzureADMSRoleAssignment.md)
Creates an Azure AD role assignment.

### [New-AzureADMSRoleDefinition](New-AzureADMSRoleDefinition.md)
Creates an Azure AD role definition.

### [New-AzureADServiceAppRoleAssignment](New-AzureADServiceAppRoleAssignment.md)
Assigns an app role to a user, a group, or another service principal.

### [New-AzureADServicePrincipal](New-AzureADServicePrincipal.md)
Creates a service principal.

### [New-AzureADServicePrincipalKeyCredential](New-AzureADServicePrincipalKeyCredential.md)
Create a new key credential for a service principal

### [New-AzureADServicePrincipalPasswordCredential](New-AzureADServicePrincipalPasswordCredential.md)
Creates a password credential for a service principal.

### [New-AzureADTrustedCertificateAuthority](New-AzureADTrustedCertificateAuthority.md)
Creates a trusted certificate authority.

### [New-AzureADUser](New-AzureADUser.md)
Creates an Azure AD user.

### [New-AzureADUserAppRoleAssignment](New-AzureADUserAppRoleAssignment.md)
Assigns a user to an application role.

### [Remove-AzureADApplication](Remove-AzureADApplication.md)
Delete an application by objectId.

### [Remove-AzureADApplicationExtensionProperty](Remove-AzureADApplicationExtensionProperty.md)
Removes an application extension property.

### [Remove-AzureADApplicationKeyCredential](Remove-AzureADApplicationKeyCredential.md)
Removes a key credential from an application.

### [Remove-AzureADApplicationOwner](Remove-AzureADApplicationOwner.md)
Removes an owner from an application.

### [Remove-AzureADApplicationPasswordCredential](Remove-AzureADApplicationPasswordCredential.md)
Removes a password credential from an application.

### [Remove-AzureADApplicationProxyApplication](Remove-AzureADApplicationProxyApplication.md)
Deletes an Application Proxy application.

### [Remove-AzureADApplicationProxyApplicationConnectorGroup](Remove-AzureADApplicationProxyApplicationConnectorGroup.md)
The Remove-AzureADApplicationProxyApplicationConnectorGroup cmdlet sets the connector group assigned for the specified application to 'Default' and removes the current assignment.

### [Remove-AzureADApplicationProxyConnectorGroup](Remove-AzureADApplicationProxyConnectorGroup.md)
The Remove-AzureADApplicationProxyConnectorGroup cmdlet deletes an Application Proxy Connector group.

### [Remove-AzureADContact](Remove-AzureADContact.md)
Removes a contact.

### [Remove-AzureADContactManager](Remove-AzureADContactManager.md)
Removes a contact's manager.

### [Remove-AzureADDeletedApplication](Remove-AzureADDeletedApplication.md)
{{ Fill in the Synopsis }}

### [Remove-AzureADDevice](Remove-AzureADDevice.md)
Deletes a device.

### [Remove-AzureADDeviceRegisteredOwner](Remove-AzureADDeviceRegisteredOwner.md)
Removes the registered owner of a device.

### [Remove-AzureADDeviceRegisteredUser](Remove-AzureADDeviceRegisteredUser.md)
Removes a registered user from a device.

### [Remove-AzureADDirectoryRoleMember](Remove-AzureADDirectoryRoleMember.md)
Removes a member of a directory role.

### [Remove-AzureADDomain](Remove-AzureADDomain.md)
Removes a domain.

### [Remove-AzureADGroup](Remove-AzureADGroup.md)
Removes a group.

### [Remove-AzureADGroupAppRoleAssignment](Remove-AzureADGroupAppRoleAssignment.md)
Delete a group application role assignment.

### [Remove-AzureADGroupMember](Remove-AzureADGroupMember.md)
Removes a member from a group.

### [Remove-AzureADGroupOwner](Remove-AzureADGroupOwner.md)
Removes an owner from a group.

### [Remove-AzureADMSAdministrativeUnit](Remove-AzureADMSAdministrativeUnit.md)
Removes an administrative unit.

### [Remove-AzureADMSAdministrativeUnitMember](Remove-AzureADMSAdministrativeUnitMember.md)
Removes an administrative unit member.

### [Remove-AzureADMSApplication](Remove-AzureADMSApplication.md)
Deletes an application object.

### [Remove-AzureADMSApplicationExtensionProperty](Remove-AzureADMSApplicationExtensionProperty.md)
Deletes an extension property from an application object.

### [Remove-AzureADMSApplicationKey](Remove-AzureADMSApplicationKey.md)
Removes a key from an application.

### [Remove-AzureADMSApplicationOwner](Remove-AzureADMSApplicationOwner.md)
Removes an owner from an application object.

### [Remove-AzureADMSApplicationPassword](Remove-AzureADMSApplicationPassword.md)
Remove a password from an application.

### [Remove-AzureADMSApplicationVerifiedPublisher](Remove-AzureADMSApplicationVerifiedPublisher.md)
Removes the verified publisher from an application.

### [Remove-AzureADMSConditionalAccessPolicy](Remove-AzureADMSConditionalAccessPolicy.md)
Deletes a conditional access policy in Azure Active Directory by Id.

### [Remove-AzureADMSDeletedDirectoryObject](Remove-AzureADMSDeletedDirectoryObject.md)
This cmdlet is used to permanently delete a previously deleted directory object

### [Remove-AzureADMSGroup](Remove-AzureADMSGroup.md)
Removes an Azure AD group.

### [Remove-AzureADMSGroupLifecyclePolicy](Remove-AzureADMSGroupLifecyclePolicy.md)
Deletes a groupLifecyclePolicies object

### [Remove-AzureADMSIdentityProvider](Remove-AzureADMSIdentityProvider.md)
This cmdlet is used to delete an identity provider in the directory.

### [Remove-AzureADMSLifecyclePolicyGroup](Remove-AzureADMSLifecyclePolicyGroup.md)
Removes a group from a lifecycle policy

### [Remove-AzureADMSNamedLocationPolicy](Remove-AzureADMSNamedLocationPolicy.md)
Deletes an Azure Active Directory named location policy by PolicyId.

### [Remove-AzureADMSPermissionGrantConditionSet](Remove-AzureADMSPermissionGrantConditionSet.md)
Delete an Azure Active Directory permission grant condition set by id

### [Remove-AzureADMSPermissionGrantPolicy](Remove-AzureADMSPermissionGrantPolicy.md)
Removes a permission grant policy.

### [Remove-AzureADMSRoleAssignment](Remove-AzureADMSRoleAssignment.md)
Removes an Azure AD role assignment.

### [Remove-AzureADMSRoleDefinition](Remove-AzureADMSRoleDefinition.md)
Removes an Azure AD role definition.

### [Remove-AzureADMSScopedRoleMembership](Remove-AzureADMSScopedRoleMembership.md)
Removes a scoped role membership.

### [Remove-AzureADMSServicePrincipalDelegatedPermissionClassification](Remove-AzureADMSServicePrincipalDelegatedPermissionClassification.md)
Remove delegated permission classification.

### [Remove-AzureADOAuth2PermissionGrant](Remove-AzureADOAuth2PermissionGrant.md)
Removes an oAuth2PermissionGrant.

### [Remove-AzureADServiceAppRoleAssignment](Remove-AzureADServiceAppRoleAssignment.md)
Removes a service principal application role assignment.

### [Remove-AzureADServicePrincipal](Remove-AzureADServicePrincipal.md)
Removes a service principal.

### [Remove-AzureADServicePrincipalKeyCredential](Remove-AzureADServicePrincipalKeyCredential.md)
Removes a key credential from a service principal.

### [Remove-AzureADServicePrincipalOwner](Remove-AzureADServicePrincipalOwner.md)
Removes an owner from a service principal.

### [Remove-AzureADServicePrincipalPasswordCredential](Remove-AzureADServicePrincipalPasswordCredential.md)
Removes a password credential from a service principal.

### [Remove-AzureADTrustedCertificateAuthority](Remove-AzureADTrustedCertificateAuthority.md)
Removes a trusted certificate authority.

### [Remove-AzureADUser](Remove-AzureADUser.md)
Removes a user.

### [Remove-AzureADUserAppRoleAssignment](Remove-AzureADUserAppRoleAssignment.md)
Removes a user application role assignment.

### [Remove-AzureADUserExtension](Remove-AzureADUserExtension.md)
Removes a user extension.

### [Remove-AzureADUserManager](Remove-AzureADUserManager.md)
Removes a user's manager.

### [Reset-AzureADMSLifeCycleGroup](Reset-AzureADMSLifeCycleGroup.md)
Renews a group by updating the RenewedDateTime property on a group to the current DateTime.

### [Restore-AzureADDeletedApplication](Restore-AzureADDeletedApplication.md)
Restores a previously deleted application

### [Restore-AzureADMSDeletedDirectoryObject](Restore-AzureADMSDeletedDirectoryObject.md)
This cmdlet is used to restore a previously deleted object.

### [Revoke-AzureADSignedInUserAllRefreshToken](Revoke-AzureADSignedInUserAllRefreshToken.md)
Invalidates the refresh tokens issued to applications for the current user.

### [Revoke-AzureADUserAllRefreshToken](Revoke-AzureADUserAllRefreshToken.md)
Invalidates the refresh tokens issued to applications for a user.

### [Select-AzureADGroupIdsContactIsMemberOf](Select-AzureADGroupIdsContactIsMemberOf.md)
Get groups in which a contact is a member.

### [Select-AzureADGroupIdsGroupIsMemberOf](Select-AzureADGroupIdsGroupIsMemberOf.md)
Gets group IDs that a group is a member of.

### [Select-AzureADGroupIdsServicePrincipalIsMemberOf](Select-AzureADGroupIdsServicePrincipalIsMemberOf.md)
Selects the groups in which a service principal is a member.

### [Select-AzureADGroupIdsUserIsMemberOf](Select-AzureADGroupIdsUserIsMemberOf.md)
Selects the groups that a user is a member of.

### [Set-AzureADApplication](Set-AzureADApplication.md)
Updates an application.

### [Set-AzureADApplicationLogo](Set-AzureADApplicationLogo.md)
Sets the logo for an Application

### [Set-AzureADApplicationProxyApplication](Set-AzureADApplicationProxyApplication.md)
The Set-AzureADApplicationProxyApplication allows you to modify and set configurations for an application in Azure Active Directory configured to use ApplicationProxy.

### [Set-AzureADApplicationProxyApplicationConnectorGroup](Set-AzureADApplicationProxyApplicationConnectorGroup.md)
The Set-AzureADApplicationProxyApplicationConnectorGroup cmdlet assigns the given connector group to a specified application.

### [Set-AzureADApplicationProxyApplicationCustomDomainCertificate](Set-AzureADApplicationProxyApplicationCustomDomainCertificate.md)
The Set-AzureADApplicationProxyApplicationCustomDomainCertificate cmdlet assigns a certificate to an application configured for Application Proxy in Azure Active Directory (AD). This will upload the certificate and allow the application to use Custom Domains.

### [Set-AzureADApplicationProxyApplicationSingleSignOn](Set-AzureADApplicationProxyApplicationSingleSignOn.md)
The Set-AzureADApplicationProxyApplicationSingleSignOn cmdlet allows you to set and modify single sign-on (SSO) settings for an application configured for Application Proxy in Azure Active Directory.

### [Set-AzureADApplicationProxyConnector](Set-AzureADApplicationProxyConnector.md)
The Set-AzureADApplicationProxyConnector cmdlet allows reassignment of the connector to another connector group.

### [Set-AzureADApplicationProxyConnectorGroup](Set-AzureADApplicationProxyConnectorGroup.md)
The Set-AzureADApplicationProxyConnectorGroup cmdlet allows you to change the name of a given Application Proxy connector group.

### [Set-AzureADDevice](Set-AzureADDevice.md)
Updates a device.

### [Set-AzureADDomain](Set-AzureADDomain.md)
Updates a domain.

### [Set-AzureADGroup](Set-AzureADGroup.md)
Updates a specific group in Azure Active Directory

### [Set-AzureADMSAdministrativeUnit](Set-AzureADMSAdministrativeUnit.md)
Updates an administrative unit.

### [Set-AzureADMSApplication](Set-AzureADMSApplication.md)
Updates the properties of an application object.

### [Set-AzureADMSApplicationLogo](Set-AzureADMSApplicationLogo.md)
Sets the logo for an application object.

### [Set-AzureADMSApplicationVerifiedPublisher](Set-AzureADMSApplicationVerifiedPublisher.md)
Sets the verified publisher of an application to a verified Microsoft Partner Network (MPN) identifier.

### [Set-AzureADMSAuthorizationPolicy](Set-AzureADMSAuthorizationPolicy.md)
Updates an authorization policy, which represents a policy that can control Azure Active Directory authorization settings.

### [Set-AzureADMSConditionalAccessPolicy](Set-AzureADMSConditionalAccessPolicy.md)
Updates a conditional access policy in Azure Active Directory by Id.

### [Set-AzureADMSGroup](Set-AzureADMSGroup.md)
Sets the properties for an existing Azure AD group.

### [Set-AzureADMSGroupLifecyclePolicy](Set-AzureADMSGroupLifecyclePolicy.md)
Updates a specific group Lifecycle Policy in Azure Active Directory

### [Set-AzureADMSIdentityProvider](Set-AzureADMSIdentityProvider.md)
This cmdlet is used to update the properties of an existing identity provider configured in the directory.

### [Set-AzureADMSNamedLocationPolicy](Set-AzureADMSNamedLocationPolicy.md)
Updates a named location policy in Azure Active Directory by PolicyId.

### [Set-AzureADMSPermissionGrantConditionSet](Set-AzureADMSPermissionGrantConditionSet.md)
Update an existing Azure Active Directory permission grant condition set.

### [Set-AzureADMSPermissionGrantPolicy](Set-AzureADMSPermissionGrantPolicy.md)
Updates a permission grant policy.

### [Set-AzureADMSRoleDefinition](Set-AzureADMSRoleDefinition.md)
Update an existing Azure AD role definition.

### [Set-AzureADServicePrincipal](Set-AzureADServicePrincipal.md)
Updates a service principal.

### [Set-AzureADTenantDetail](Set-AzureADTenantDetail.md)
Set contact details for a tenant

### [Set-AzureADTrustedCertificateAuthority](Set-AzureADTrustedCertificateAuthority.md)
Updates a trusted certificate authority.

### [Set-AzureADUser](Set-AzureADUser.md)
Updates a user.

### [Set-AzureADUserExtension](Set-AzureADUserExtension.md)
Sets a user extension.

### [Set-AzureADUserLicense](Set-AzureADUserLicense.md)
Adds or removes licenses for a Microsoft online service to the list of assigned licenses for a user.

### [Set-AzureADUserManager](Set-AzureADUserManager.md)
Updates a user's manager.

### [Set-AzureADUserPassword](Set-AzureADUserPassword.md)
Sets the password of a user.

### [Set-AzureADUserThumbnailPhoto](Set-AzureADUserThumbnailPhoto.md)
Set the thumbnail photo for a user

### [Update-AzureADSignedInUserPassword](Update-AzureADSignedInUserPassword.md)
Updates the password for the signed-in user.
