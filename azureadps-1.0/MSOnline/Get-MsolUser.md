---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: CED5BB55-E2BA-4400-9777-6589B6B29355
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolUser

## SYNOPSIS
Gets users from Azure Active Directory.

## SYNTAX

### ListUsers__0 (Default)
```
Get-MsolUser [-ReturnDeletedUsers] [-City <String>] [-Country <String>] [-Department <String>]
 [-DomainName <String>] [-EnabledFilter <UserEnabledFilter>] [-State <String>] [-Synchronized]
 [-Title <String>] [-HasErrorsOnly] [-LicenseReconciliationNeededOnly] [-UnlicensedUsersOnly]
 [-UsageLocation <String>] [-SearchString <String>] [-MaxResults <Int32>] [-TenantId <Guid>]
 [<CommonParameters>]
```

### GetUser__0
```
Get-MsolUser -ObjectId <Guid> [-ReturnDeletedUsers] [-TenantId <Guid>] [<CommonParameters>]
```

### GetUserByUpn__0
```
Get-MsolUser [-ReturnDeletedUsers] -UserPrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolUser [-ReturnDeletedUsers] [-City <String>] [-Country <String>] [-Department <String>]
 [-DomainName <String>] [-EnabledFilter <UserEnabledFilter>] [-State <String>] [-Synchronized]
 [-Title <String>] [-HasErrorsOnly] [-LicenseReconciliationNeededOnly] [-UnlicensedUsersOnly]
 [-UsageLocation <String>] [-SearchString <String>] [-All] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolUser** cmdlet gets an individual user or list of users.
Specify the _ObjectId_ or _UserPrincipalName_ parameter to get a specific user.

## EXAMPLES

### Example 1: Get all users
```
PS C:\> Get-MsolUser
```

This command retrieves all users in the company.
It displays up to the default value of 500 results.

### Example 2: Get enabled users
```
PS C:\> Get-MsolUser -EnabledFilter EnabledOnly -MaxResults 2000
```

This command gets up to 2000 enabled users.

### Example 3: Get a user by UPN
```
PS C:\> Get-MsolUser -UserPrincipalName "davidchew@contoso.com"
```

This command retrieves the user with the UPN davidchew@contoso.com.

### Example 4: Get a user by object ID
```
PS C:\> Get-MsolUser -ObjectId 81701046-cb37-439b-90ce-2afd9630af7d
```

This command retrieves a user that has the specified object ID.

### Example 5: Get users by search String
```
PS C:\> Get-MsolUser -SearchString "David"
```

This command retrieves a list of users with David in the display name or email address.

### Example 6: Get preferred data location of a user
```
PS C:\> Get-MsolUser -UserPrincipalName "davidchew@contoso.onmicrosoft.com" | Select PreferredDataLocation
```

This command returns the preferred data location of a user.

## PARAMETERS

### -All
Indicates that this cmdlet returns all results.
Do not specify together with the _MaxResults_ parameter.

```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -City
Specifies the city to filter results on.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Country
Specifies the country to filter results on.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Department
Specifies the department to filter results on.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName
Specifies the domain to filter results on.
This must be a verified domain for the company.
All users with an email address, primary or secondary, on this domain is returned.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledFilter
Specifies the filter for enabled or disabled users.
Valid values are All, EnabledOnly, and DisabledOnly.

```yaml
Type: UserEnabledFilter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HasErrorsOnly
Inidates that this cmdlet returns only users that have validation errors.

```yaml
Type: SwitchParameter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseReconciliationNeededOnly
Indicates that this cmdlet filter for only users that require license reconciliation.

```yaml
Type: SwitchParameter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.
The default value is 500.

```yaml
Type: Int32
Parameter Sets: ListUsers__0
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the user to get.

```yaml
Type: Guid
Parameter Sets: GetUser__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReturnDeletedUsers
Indicates that this cmdlet returns only users in the recycling bin.

```yaml
Type: SwitchParameter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetUser__0, GetUserByUpn__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
Specifies a string to match email address or display name starting with this string.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Specifies the filter for the state of the user.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Synchronized
Indicates that this cmdlet returns only users who are synchronized through Azure Active Directory Sync.

```yaml
Type: SwitchParameter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Title
Speicifies the filter for the title of the user.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnlicensedUsersOnly
Indicates that this cmdlet returns only users who are not assigned a license.

```yaml
Type: SwitchParameter
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageLocation
Specifies the filter for the country where the services are consumed by the user.
Specify a two-letter country code.

```yaml
Type: String
Parameter Sets: ListUsers__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
Speicifies the user ID of the user to retrieve.

```yaml
Type: String
Parameter Sets: GetUserByUpn__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.User
This cmdlet returns user objects, which include the following information:

* AlternateEmailAddresses. Alternate email address of the user (external to Azure Active Directory).

* BlockCredential. Whether or not the user is able to sign in.

* City. The user's city.

* Country. The user's country.

* Department. The user's department.

* DisplayName. The user's display name.

* Errors. An array of errors.
These are validation errors that may result in loss of services.

* Fax. The user's fax number.

* FirstName. The user's first name.

* ImmutableID. Only returned for federated users.
This is the ID that is required to be federated with Azure Active Directory.

* isBlackBerryUser. Returns whether or not the user has a BlackBerry device.

* isLicensed. Whether or not the user has any licenses assigned.

* LastDirSyncTime. The date and time of the last directory synchronization (only returned from users synced with Azure Active Directory through Active Directory synchronization).

* LastPasswordChangeTimestamp. The most recent time at which a password change for the user was registered in Azure Active Directory.

* LastName. The user's last name.

* LicenseReconciliationNeeded. Whether or not the user currently has a mailbox without a license.
In this case, the user should be licensed with 30 days to avoid losing their mailbox.

* Licenses. A list of the user's licenses.

* LiveID. The user's unique login ID.

* MobilePhone. The user's mobile phone number.

* ObjectId. The user's unique ID.

* Office. The user's office number.

* OverallProvisioningStatus. Whether or not the user has been provisioned for their services.

* PasswordNeverExpires. Whether the user's password should be forced to change every 90 days.

* Phone Number. The user's phone number.

* Postal Code. The user's postal code.

* Preferred Data Location. The user's preferred data location.

* Preferred Language. The user's preferred language.

* Proxy Addresses. The proxy addresses associated with this user.

* State. The user's state.

* StreetAddress. The user's street address.

* StrongPasswordRequired. Whether the user is required to set a strong password when they change their password.
Strong passwords are recommended.

* Title. The user's title.

* UsageLocation. The country where the services are consumed by the user.
This must be a two letter country code.

* UserPrincipalName. The user ID of the user.

* ValidationStatus. Whether or not the user has any errors.

## NOTES

## RELATED LINKS
[New-MsolUser](./New-MsolUser.md)

[Remove-MsolUser](./Remove-MsolUser.md)

[Restore-MsolUser](./Restore-MsolUser.md)

[Set-MsolUser](./Set-MsolUser.md)
