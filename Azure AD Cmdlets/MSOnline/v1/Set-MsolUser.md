---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: F0BE5738-B797-4F9E-B963-73155997618F
---

# Set-MsolUser

## SYNOPSIS
Updates a user in Microsoft Azure Active Directory.

## SYNTAX

```
Set-MsolUser [-ImmutableId <String>] [-ObjectId <Guid>] [-UserPrincipalName <String>]
 [-BlockCredential <Boolean>] [-City <String>] [-Country <String>] [-Department <String>]
 [-DisplayName <String>] [-Fax <String>] [-FirstName <String>] [-LastName <String>]
 [-LastPasswordChangeTimestamp <DateTime>] [-MobilePhone <String>] [-Office <String>]
 [-PasswordNeverExpires <Boolean>] [-PhoneNumber <String>] [-PostalCode <String>]
 [-PreferredDataLocation <String>] [-PreferredLanguage <String>] [-SoftDeletionTimestamp <DateTime>]
 [-State <String>] [-StreetAddress <String>] [-StrongPasswordRequired <Boolean>] [-Title <String>]
 [-UsageLocation <String>] [-AlternateEmailAddresses <String[]>]
 [-StrongAuthenticationMethods <StrongAuthenticationMethod[]>] [-AlternateMobilePhones <String[]>]
 [-StrongAuthenticationRequirements <StrongAuthenticationRequirement[]>]
 [-StsRefreshTokensValidFrom <DateTime>] [-UserType <UserType>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolUser cmdlet is used to update a user object.

        Note that this cmdlet should be used for basic properties only.
The licenses, password, and User Principal Name for a user can be updated through the Set-MsolUserLicense, Set-MsolUserPassword and Set-MsolUserPrincipalName cmdlets respectively.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Set-MsolUser -UserPrincipalName user@contoso.com -blockcredential $true

          None
```

Description

-----------

This command sets block credential to true for a user (which will block them from being able to sign in). 
This cannot be set for a synced user.

### -------------------------- EXAMPLE 2 --------------------------
```
Set-MsolUser -UserPrincipalName user@contoso.com -DisplayName "John Doe" -Title "Manager" -Department "Finance"

          None
```

Description

-----------

This command updates the display name for the specified user.

### -------------------------- EXAMPLE 3 --------------------------
```
Set-MsolUser -UserPrincipalName user@contoso.com -UsageLocation "CA"

          None
```

Description

-----------

This command sets the location (country) of this user.
The country must be a two-letter ISO code.
This can be set for synced users as well as managed users.

### -------------------------- EXAMPLE 4 --------------------------
```
Set-MsolUser -UserPrincipalName john@contoso.onmicrosoft.com -PreferredDataLocation EUR

          None
```

Description

-----------

This command sets the preferred data location property of a user whose user principal name is john@contoso.onmicrosoft.com to EUR.

## PARAMETERS

### -AlternateEmailAddresses
Alternate email addresses of the user.

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
Alternate mobile phone numbers of the user.

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
When true, the user will not be able to sign in using their user ID.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
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
The country or region of the user.

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

### -ObjectId
The unique ID of the user.

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

### -Office
The location of the office of the user.

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
Default value: None
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
The postal code for the user's location.

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
The state or province where the user is located.

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
Default value: None
Accept pipeline input: True (ByPropertyName)
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
The user ID of the user.

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

## NOTES

## RELATED LINKS


