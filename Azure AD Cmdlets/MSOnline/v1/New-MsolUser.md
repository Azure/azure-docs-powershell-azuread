---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 1E77AB39-65ED-4280-A4EF-09F323C0D341
---

# New-MsolUser

## SYNOPSIS
Adds a new user to Microsoft Azure Active Directory.

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
The New-MsolUser cmdlet is used to create a new user in Microsoft Azure Active Directory.
In order to give the user access to services, they must also be assigned a license (using the LicenseAssignment parameter).

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
New-MsolUser -UserPrincipalName user@contoso.com -DisplayName "John Doe" -FirstName "John" -LastName "Doe"

          Returns a user object.
```

Description

-----------

This command creates a new user. 
The user will not have any licenses assigned. 
A random password will be generated for the user.

### -------------------------- EXAMPLE 2 --------------------------
```
New-MsolUser -UserPrincipalName user@contoso.com -DisplayName "John Doe" -FirstName "John" -LastName "Doe" -UsageLocation "US" -LicenseAssignment "Contoso:BPOS_Standard"

          Returns a user object.
```

Description

-----------

This command creates a new user and assigns them a license.

### -------------------------- EXAMPLE 3 --------------------------
```
New-MsolUser -UserPrincipalName john@contoso.onmicrosoft.com -DisplayName John -PreferredDataLocation EUR

          Returns a user object.
```

Description

-----------

This command creates a user whose user principal name is john@contoso.onmicrosoft.com, display name is John, and preferred data location is EUR.

## PARAMETERS

### -AlternateEmailAddresses
The alternate email addresses of the user.

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
Alternate mobile phone numbers of the user

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
When true, the user will not be able to log on using their user ID.

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
The city of the user.

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
The country of the user.

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
The department of the user.

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
The display name of the user.

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
The fax number of the user.

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
The first name of the user.

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
When true, the user will be required to change their password the next time they sign in.

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
The immutable ID of the user's federated identity.
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
The last name of the user.

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
List of licenses to assign the user.

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
License options for license assignment.
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
The mobile phone number of the user.

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
The office of the user.

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
The new password for the user.
If the user is set to require a strong password, then all of the following rules must be met:
            - The password must contain at least one lowercase letter
            - The password must contain at least one uppercase letter
            - The password must contain at least one non-alphanumeric character
            - The password cannot contain any spaces, tabs, or line breaks
            - The length of the password must be 8-16 characters
            - The user name cannot be contained in the password

            If this value is omitted, then a random password will be assigned to the user.

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
Sets whether or not the user's password will expire periodically.

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
The phone number of the user.

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
The postal code of the user.

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
The preferred data location to set for the user.

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
The preferred language of the user.

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
The state where the user is located.

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
The street address of the user.

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
Sets whether or not the user requires a strong password.

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
The title of the user.

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
The location of the user where services are consumed.
Must be a two-letter country code.

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
The user ID for this user.
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


