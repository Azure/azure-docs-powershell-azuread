---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADUser

## SYNOPSIS
Updates a specific user in Azure Active Directory

## SYNTAX

```
Set-AzureADUser -ObjectId <String> [-ExtensionProperty <Dictionary`2[String]>]
 [-AccountEnabled <Nullable`1[Boolean]>] [-AssignedLicenses <List`1[AssignedLicense]>] [-City <String>]
 [-Country <String>] [-Department <String>] [-DisplayName <String>] [-FacsimilieTelephoneNumber <String>]
 [-GivenName <String>] [-ImmutableId <String>] [-JobTitle <String>] [-Mail <String>] [-MailNickName <String>]
 [-Mobile <String>] [-OtherMails <List`1[String]>] [-PasswordPolicies <String>]
 [-PasswordProfile <PasswordProfile>] [-PhysicalDeliveryOfficeName <String>] [-PostalCode <String>]
 [-PreferredLanguage <String>] [-State <String>] [-StreetAddress <String>] [-Surname <String>]
 [-TelephoneNumber <String>] [-ThumbnailPhoto <Byte[]>] [-UsageLocation <String>] [-UserPrincipalName <String>]
 [-UserType <String>]
```

## DESCRIPTION

## EXAMPLES

### Set the display name of a user
```
$UserId = (Get-AzureADUser - Top 1).ObjectId
Set-AzureADUser -ObjectId $UserId -DisplayName = 'YetAnotherTestUser
```

## PARAMETERS

### -ObjectId
The unique identifier of a user in Azure Active Directory (UPN or ObjectId)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionProperty
@{Text=}

```yaml
Type: Dictionary`2[String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountEnabled
true if the account is enabled; otherwise, false.
This property is required when a user is created.

```yaml
Type: Nullable`1[Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignedLicenses
The licenses that are assigned to the user.
This is a collection of AssignedLicenses objects.
more information can be found here: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/entity-and-complex-type-reference#assignedlicense-type

```yaml
Type: List`1[AssignedLicense]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -City
The city in which the user is located.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Country
The country/region in which the user is located; for example, "US" or "UK".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Department
The name for the department in which the user works.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
The name displayed in the address book for the user.
This is usually the combination of the user's first name, middle initial and last name.
This property is required when a user is created and it cannot be cleared during updates.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FacsimilieTelephoneNumber
The telephone number of the user's business fax machine.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GivenName
The given name (first name) of the user.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImmutableId
This property is used to associate an on-premises Active Directory user account to their Azure AD user object.
This property must be specified when creating a new user account in the Graph if you are using a federated domain for the user's userPrincipalName (UPN) property.

Important: The $ and _ characters cannot be used when specifying this property.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobTitle
The user's job title.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mail
The SMTP address for the user, for example, "jeff@contoso.onmicrosoft.com".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailNickName
The mail alias for the user.
This property is required when you create a work or school account; it is optional for a local account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mobile
The mail alias for the user.
This property is required when you create a work or school account; it is optional for a local account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OtherMails
A list of additional email addresses for the user; for example: \["bob@contoso.com", "Robert@fabrikam.com"\].

Notes: not nullable, the any operator is required for filter expressions on multi-valued properties

```yaml
Type: List`1[String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordPolicies
Specifies password policies for the user.
This value is an enumeration with one possible value being "DisableStrongPassword", which allows weaker passwords than the default policy to be specified.
"DisablePasswordExpiration" can also be specified.
The two may be specified together; for example: "DisablePasswordExpiration, DisableStrongPassword".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordProfile
Specifies the password profile for the user.
The profile contains the user's password.
This property is required when a user is created.

Note that the -PasswordProfile attribute requires an object of the type Microsoft.Open.AzureAD.Model.PasswordProfile

The password in the profile must satisfy minimum requirements as specified by the passwordPolicies property.
By default, a strong password is required.
For information about the constraints that must be satisfied for a strong password, see Password policy under Change your password in the Microsoft Office 365 help pages.

```yaml
Type: PasswordProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhysicalDeliveryOfficeName
The office location in the user's place of business.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostalCode
The postal code for the user's postal address.
The postal code is specific to the user's country/region.
In the United States of America, this attribute contains the ZIP code.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferredLanguage
The preferred language for the user.
Should follow ISO 639-1 Code; for example "en-US".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
The state or province in the user's address.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StreetAddress
The street address of the user's place of business

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Surname
The user's surname (family name or last name).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TelephoneNumber
The primary telephone number of the user's place of business.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThumbnailPhoto
A thumbnail photo to be displayed for the user.

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageLocation
A two letter country code (ISO standard 3166).
Required for users that will be assigned licenses due to legal requirement to check for availability of services in countries.
Examples include: "US", "JP", and "GB".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
The user principal name (UPN) of the user.
The UPN is an Internet-style login name for the user based on the Internet standard RFC 822.
By convention, this should map to the user's email name.
The general format is "alias@domain".
For work or school accounts, the domain must be present in the tenant's collection of verified domains.
This property is required when a work or school account is created; it is optional for local accounts. 

The verified domains for the tenant can be accessed from the VerifiedDomains property of TenantDetail.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserType
A string value that can be used to classify user types in your directory, such as "Member" and "Guest".

```yaml
Type: String
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

