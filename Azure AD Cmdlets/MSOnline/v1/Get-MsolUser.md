---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: CED5BB55-E2BA-4400-9777-6589B6B29355
---

# Get-MsolUser

## SYNOPSIS
Retrieves a user from Microsoft Azure Active Directory.

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
The Get-MsolUser cmdlet can be used to retrieve an individual user, or list of users.
An individual user will be retrieved if the ObjectId or UserPrincipalName parameter is used.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolUser

          Returns a list of users.
```

Description

-----------

This command retrieves all users in the company (up to 500 results).

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MsolUser -EnabledFilter EnabledOnly -MaxResults 2000

          Returns a list of users.
```

Description

-----------

This command retrieves a list of enabled users (up to 2000 results).

### -------------------------- EXAMPLE 3 --------------------------
```
Get-MsolUser -UserPrincipalName johns@contoso.com

          Returns a user object.
```

Description

-----------

This command retrieves the user with the UPN johns@contoso.com

### -------------------------- EXAMPLE 4 --------------------------
```
Get-MsolUser -ObjectId <guid>

          Returns a user object.
```

Description

-----------

This command retrieves a user with the corresponding object ID.

### -------------------------- EXAMPLE 5 --------------------------
```
Get-MsolUser -SearchString "Tim"

          Returns a user object.
```

Description

-----------

This command retrieves a list of users with "Tim" in the display name or email address (up to 500 results).

### -------------------------- EXAMPLE 6 --------------------------
```
Get-MsolUser -EnabledFilter EnabledOnly -MaxResults 2000

          None
```

Description

-----------

This command retrieves a list of enabled users (up to 2000 results).

### -------------------------- EXAMPLE 7 --------------------------
```
Get-MsolUser -UserPrincipalName john@contoso.onmicrosoft.com | Select PreferredDataLocation
```

Description

-----------

This command returns the preferred data location of a user.

## PARAMETERS

### -All
If present, then all results will be returned.
Cannot be used with MaxResults parameter.

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
The city to filter results on.

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
The country to filter results on.

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
The department to filter results on.

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
The domain to filter results on.
This must be a verified domain for the company.
All users with an email address (primary or secondary) on this domain will be returned.

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
The filter for enabled (or disabled) users.
Possible values are All, EnabledOnly, and DisabledOnly.

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
The filter for only users with validation errors.

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
The filter for only users that require license reconciliation.

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
The maximum number of results returned for a search result.
If not specified, 500 results will be returned.

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
The unique ID of the user to retrieve.

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
If set, only users in the recycling bin will be deleted.

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
The string to search for users.
Only users with an email address or display name starting with this string will be returned.

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
The filter for the user's state.

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
The filter for only users who are synchronized through Microsoft Azure Active Directory Sync.

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
The unique ID of the tenant to perform the operation on.
If this is not provided, then the value will default to the tenant of the current user.
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

### -Title
The filter for the user's title.

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
The filter for only users who are not assigned a license.

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
The filter for the country where the services are consumed by the user.
This must be a two-letter country code.

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
The user ID of the user to retrieve.

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

            AlternateEmailAddresses: Alternate email address of the user (external to Microsoft Azure Active Directory).

            BlockCredential: Whether or not the user is able to sign in.

            City: The user's city.

            Country: The user's country.

            Department: The user's department.

            DisplayName: The user's display name.

            Errors: An array of errors.
These are validation errors that may result in loss of services.

            Fax: The user's fax number.

            FirstName: The user's first name.

            ImmutableID: Only returned for federated users.
This is the ID that is required to be federated with Microsoft Azure Active Directory.

            isBlackBerryUser: Returns whether or not the user has a BlackBerry device.

            isLicensed: Whether or not the user has any licenses assigned.

            LastDirSyncTime: The date and time of the last directory synchronization (only returned from users synced with Microsoft Azure Active Directory through Active Directory synchronization).

            LastPasswordChangeTimestamp: The most recent time at which a password change for the user was registered in Microsoft Azure Active Directory.

            LastName: The user's last name.

            LicenseReconciliationNeeded: Whether or not the user currently has a mailbox without a license.
In this case, the user should be licensed with 30 days to avoid losing their mailbox.

            Licenses: A list of the user's licenses.

            LiveID: The user's unique login ID.

            MobilePhone: The user's mobile phone number.

            ObjectId: The user's unique ID.

            Office: The user's office number.

            OverallProvisioningStatus: Whether or not the user has been provisioned for their services.

            PasswordNeverExpires: Whether the user's password should be forced to change every 90 days.

            Phone Number: The user's phone number.

            Postal Code: The user's postal code.

            Preferred Data Location: The user's preferred data location.

            Preferred Language: The user's preferred language.

            Proxy Addresses - the proxy addresses associated with this user.

            State: The user's state.

            StreetAddress: The user's street address.

            StrongPasswordRequired: Whether the user is required to set a strong password when they change their password.
Strong passwords are recommended.

            Title: The user's title.

            UsageLocation: The country where the services are consumed by the user.
This must be a two letter country code.

            UserPrincipalName: The user ID of the user.

            ValidationStatus: Whether or not the user has any errors.

## NOTES

## RELATED LINKS


