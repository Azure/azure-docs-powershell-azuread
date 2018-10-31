---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: BC3EA621-0115-4312-B856-02AC82DB9F4E
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolCompanyInformation

## SYNOPSIS
Gets company-level information.

## SYNTAX

```
Get-MsolCompanyInformation [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolCompanyInformation** cmdlet gets company-level information.

## EXAMPLES

### Example 1: Get company-level information
```
PS C:\> Get-MsolCompanyInformation
```

This command gets company-level information.

## PARAMETERS

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.CompanyInformation
This cmdlet returns the following company level information:

* AuthorizedServiceInstances. A list of the services for this company.

* City. The company's city.

* CompanyType. What type of company this is (can be partner or regular tenant).

* Country. The company's country.

* CountryLetterCode. The two letter code for the company's country.

* DapEnabled. For partners, whether or not this partner had delegated administrator privileges.

* DirectorySynchronizationEnabled. When true, this company has directory synchronization turned on.

* DirSyncServiceAccount. The UserPrincipalName of the Global Administrator that is configured for directory synchronization.

* DisplayName. The display name of this company.

* InitialDomain. The initial domain of this company (companyname.onmicrosoft.com).

* LastDirSyncTime. The last time that directory synchronization was run for this company.

* LastPasswordSyncTime. The last time that password sync request was received for the company.

* PasswordSynchronizationEnabled. When true, this company has password synchronization turned on.

* MarketingNotificationEmails. The email address to send marketing notifications to.

* ObjectId. The unique ID for the company.

* PostalCode. The company's postal location.

* PreferredLanguage. The default language for the company.

* State. The company's state.

* Street. The company's street address.

* TechnicalNotificationEmails. The email address to send important notifications to.
This includes any directory synchronization notifications.

* TelephoneNumber. The telephone number for the company.

* UsersPermissionToCreateGroupsEnabled. The setting to allow users permission to create groups.

* UsersPermissionToCreateLOBAppsEnabled. The setting to allow users to create LOB applications.

* UsersPermissionToReadOtherUsersEnabled. The setting to allow users to read other users.

* UsersPermissionToUserConsentToAppEnabled. The setting to allow users to user consent to applications.

## NOTES

## RELATED LINKS
