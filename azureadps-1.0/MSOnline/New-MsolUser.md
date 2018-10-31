---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 1E77AB39-65ED-4280-A4EF-09F323C0D341
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-MsolUser

## SYNOPSIS
Creates a user to Azure Active Directory.

## SYNTAX

```
New-MsolUser [-ImmutableId <String>] [-UserPrincipalName <String>] [-BlockCredential <Boolean>]
 [-City <String>] [-Country <String>] [-Department <String>] [-DisplayName <String>] [-Fax <String>]
 [-FirstName <String>] [-LastName <String>] [-LastPasswordChangeTimestamp <DateTime>] [-MobilePhone <String>]
 [-Office <String>] [-PasswordNeverExpires <Boolean>] [-PhoneNumber <String>] [-PostalCode <String>]
 [-PreferredDataLocation <String>] [-PreferredLanguage <String>] [-SoftDeletionTimestamp <DateTime>]
 [-State <String>] [-StreetAddress <String>] [-StrongPasswordRequired <Boolean>] [-Title <String>]
 [-UsageLocation <String>] [-AlternateEmailAddresses <String[]>]
 [-StrongAuthenticationMethods <StrongAuthenticationMethod[]>] [-AlternateMobilePhones <String[]>]
 [-StrongAuthenticationRequirements <StrongAuthenticationRequirement[]>]
 [-StsRefreshTokensValidFrom <DateTime>] [-UserType <UserType>] [-Password <String>]
 [-LicenseOptions <LicenseOption[]>] [-ForceChangePassword <Boolean>] [-LicenseAssignment <String[]>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MsolUser** cmdlet creates a user in Azure Active Directory.
In order to give the user access to services, assign a license by using the _LicenseAssignment_ parameter.

## EXAMPLES

### Example 1: Create a user
```
PS C:\> New-MsolUser -UserPrincipalName "davidchew@contoso.com" -DisplayName "David Chew" -FirstName "David" -LastName "Chew"
```

This command creates a user.
The user does not have any licenses assigned.
A random password is generated for the user.

### Example 2: Create a user and assign a license
```
PS C:\> New-MsolUser -UserPrincipalName "davidchew@contoso.com" -DisplayName "David Chew" -FirstName "David" -LastName "Chew" -UsageLocation "US" -LicenseAssignment "Contoso:BPOS_Standard"
```

This command creates a new user and assigns a license.

### Example 3: Create a user and a preferred data location
```
PS C:\> New-MsolUser -UserPrincipalName "davidchew@contoso.onmicrosoft.com" -DisplayName "David" -PreferredDataLocation "EUR"
```

This command creates a user whose user principal name is jdavidchew@contoso.onmicrosoft.com, display name is David, and preferred data location is EUR.

## PARAMETERS

### -AlternateEmailAddresses
Specifies alternate email addresses for the user.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AlternateMobilePhones
Specifies alternate mobile phone numbers for the user.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BlockCredential
Specifies whether the user is not able to log on using their user ID.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -City
Specifies the city of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Country
Specifies the country of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Department
Specifies the department of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Specifies the display name of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fax
Specifies the fax number of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirstName
Specifies the first name of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePassword
Indicates that the user is required to change their password the next time they sign in.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $true
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImmutableId
Specifies the immutable ID of the federated identity of the user.
This should be omitted for users with standard identities.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Specifies the last name of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseAssignment
Specifies an array of licenses to assign the user.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseOptions
Specifies the options for license assignment.
Used to selectively disable individual service plans within a SKU.

```yaml
Type: LicenseOption[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MobilePhone
Specifies the mobile phone number of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Office
Specifies the office of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Specifies the new password for the user.
If the user is set to require a strong password, then all of the following rules must be met:

- The password must contain at least one lowercase letter
- The password must contain at least one uppercase letter
- The password must contain at least one non-alphanumeric character
- The password cannot contain any spaces, tabs, or line breaks
- The length of the password must be 8-16 characters
- The user name cannot be contained in the password

If this value is omitted, then a random password is assigned to the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordNeverExpires
Specifies whether the user password expires periodically.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PhoneNumber
Specifies the phone number of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PostalCode
Specifies the postal code of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PreferredDataLocation
Specifies the preferred data location for the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PreferredLanguage
Specifies the preferred language of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Specifies the state or province where the user is located.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StreetAddress
Specifies the street address of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StrongPasswordRequired
Specifies whether to require a strong password for the user.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $true
Accept pipeline input: True (ByPropertyName)
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
Specifies the title of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UsageLocation
Specifies the location of the user where services are consumed.
Specify a two-letter country code.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Specifies the user ID for this user.
This is required.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastPasswordChangeTimestamp
Specifies a time when the password was last changed.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SoftDeletionTimestamp
Specifies a time for soft deletion.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StrongAuthenticationMethods
Specifies an array of strong authentication methods.


```yaml
Type: StrongAuthenticationMethod[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StrongAuthenticationRequirements
Specifies an array of strong authentication requirements.

```yaml
Type: StrongAuthenticationRequirement[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StsRefreshTokensValidFrom
Specifies a StsRefreshTokensValidFrom value.


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserType
Specifies the user type.

```yaml
Type: UserType
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

### Microsoft.Online.Administration.User
This cmdlet returns details about the new user that was created, including their temporary password.

## NOTES

## RELATED LINKS
[Get-MsolUser](./Get-MsolUser.md)

[Remove-MsolUser](./Remove-MsolUser.md)

[Restore-MsolUser](./Restore-MsolUser.md)

[Set-MsolUser](./Set-MsolUser.md)
