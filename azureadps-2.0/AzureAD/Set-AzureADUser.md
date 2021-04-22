---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADUser

## SYNOPSIS
Updates a user.

## SYNTAX

```
Set-AzureADUser -ObjectId <String>
 [-ExtensionProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AccountEnabled <Boolean>] [-AgeGroup <String>] [-City <String>] [-CompanyName <String>]
 [-ConsentProvidedForMinor <String>] [-Country <String>] [-CreationType <String>] [-Department <String>]
 [-DisplayName <String>] [-FacsimileTelephoneNumber <String>] [-GivenName <String>] [-IsCompromised <Boolean>]
 [-ImmutableId <String>] [-JobTitle <String>] [-MailNickName <String>] [-Mobile <String>]
 [-OtherMails <System.Collections.Generic.List`1[System.String]>] [-PasswordPolicies <String>]
 [-PasswordProfile <PasswordProfile>] [-PhysicalDeliveryOfficeName <String>] [-PostalCode <String>]
 [-PreferredLanguage <String>] [-ShowInAddressList <Boolean>]
 [-SignInNames <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.SignInName]>] [-State <String>]
 [-StreetAddress <String>] [-Surname <String>] [-TelephoneNumber <String>] [-UsageLocation <String>]
 [-UserPrincipalName <String>] [-UserState <String>] [-UserStateChangedOn <String>] [-UserType <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADUser cmdlet updates a user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Update a user
```
PS C:\> $user = Get-AzureADUser -ObjectId TestUser@example.com 
PS C:\> $user.DisplayName = 'YetAnotherTestUser' 
PS C:\> Set-AzureADUser -ObjectId TestUser@example.com -Displayname $user.Displayname
```

### Example 2: Set all but speciified users as minors with parental consent
```pwsh
Get-AzureADUser -All $true | 
Where-Object -FilterScript { $_.DisplayName -notmatch '(George|James|Education)' } | ForEach-Object  { Set-AzureADUser -ObjectId $($_.ObjectId) -AgeGroup 'minorWithParentalConsent' -ConsentProvidedForMinor 'granted' }
```

This command updates the specified user's property.

## PARAMETERS

### -AccountEnabled
Indicates whether the account is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -City
Specifies the user's city.

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
Specifies the user's country.

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

### -CreationType
Indicates whether the user account is a local account for an Azure Active Directory B2C tenant.
Possible values are "LocalAccount" and null.
When creating a local account, the property is required and you must set it to "LocalAccount".
When creating a work or school account, do not specify the property or set it to null.

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
Specifies the user's department.

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
Specifies the user's display name.

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

### -ExtensionProperty

Add data to custom user properties as the basic **open extensions** or the more versatile **schema extensaions**. See [more about extensions][Learn more about extensions].

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GivenName
Specifies the user's given name.

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
This property is used to associate an on-premises Active Directory user account to their Azure AD user object. This property must be specified when creating a new user account in the Graph if you are using a federated domain for the user's `userPrincipalName` (UPN) property. **Important:** The **$** and **\_** characters cannot be used when specifying this property.

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

### -IsCompromised
True if this user is compromised

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobTitle
Specifies the user's job title.

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
Specifies a nickname for the user's mail address.

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
Specifies the user's mobile phone number.

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

### -ObjectId
Specifies the ID of a user (as a UPN or ObjectId) in Azure AD.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -OtherMails
Specifies other email addresses for the user.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Specifies the user's password profile.

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
The office location in the user's place of business. Maximum length is 128 characters.

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
Specifies the user's postal code.

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
Specifies the user's preferred language.

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

### -ShowInAddressList
Set to True to show this user in the address list.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInNames
The list of sign in names for this user

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.SignInName]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Specifies the user's state.

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
Specifies the user's street address.

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
Specifies the user's surname.

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
Specifies the user's telephone number.

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

### -UsageLocation
A two letter country code ([ISO standard 3166](https://www.iso.org/iso-3166-country-codes.html)). Required for users that will be assigned licenses due to legal requirement to check for availability of services in countries.  Examples include: "US", "JP", and "GB". Not nullable. 

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
Specifies the user's user principal name.

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

### -FacsimileTelephoneNumber
 The fax number of the user.

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

### -AgeGroup
Used by enterprise applications to determine the legal age group of the user. This property is read-only and calculated based on **ageGroup** and **consentProvidedForMinor** properties. Allowed values: `null`, `minor`, `notAdult` and `adult`. Refer to the [legal age group property definitions][Learn more about age group and minor consent definitions].

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

### -CompanyName
The company name which the user is associated. This property can be useful for describing the company that an external user comes from. The maximum length of the company name is 64 characters.

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

### -ConsentProvidedForMinor
Sets whether consent has been obtained for minors. Allowed values: `null`, `granted`, `denied` and `notRequired`. Refer to the [legal age group property definitions][Learn more about age group and minor consent definitions] for further information. 

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

### -UserState
For an external user invited to the tenant using the [invitation API](https://docs.microsoft.com/en-us/graph/api/invitation-post), this property represents the invited user's invitation status. For invited users, the state can be `PendingAcceptance` or `Accepted`, or `null` for all other users.

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

### -UserStateChangedOn
Shows the timestamp for the latest change to the externalUserState property.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUser]()

[New-AzureADUser]()

[Remove-AzureADUser]()

[Learn more about age group and minor consent definitions]: https://docs.microsoft.com/en-us/graph/api/resources/user?view=graph-rest-1.0#legal-age-group-property-definitions

[Learn more about extensions]: https://docs.microsoft.com/en-us/graph/extensibility-overview
