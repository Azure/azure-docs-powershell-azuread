---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: F0BE5738-B797-4F9E-B963-73155997618F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolUser

## SYNOPSIS
Modifies a user in Azure Active Directory.

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
The **Set-MsolUser** cmdlet modifies a user object.

Use this cmdlet only for updates to basic properties.
Update the licenses, password, and User Principal Name for a user by using the [Set-MsolUserLicense](./Set-MsolUserLicense.md), [Set-MsolUserPassword](./Set-MsolUserPassword.md) and [Set-MsolUserPrincipalName](./Set-MsolUserPrincipalName.md) cmdlets.

## EXAMPLES

### Example 1: Block credential for a user
```
PS C:\> Set-MsolUser -UserPrincipalName "davidchew@contoso.com" -BlockCredential $True
```

This command sets block credential to $True for a user, which blocks them from being able to sign in.
This cannot be done for a synced user.

### Example 2: Update display name
```
PS C:\> Set-MsolUser -UserPrincipalName "davidchew@contoso.com" -DisplayName "David Chew" -Title "Manager" -Department "Finance"
```

This command updates the display name for the specified user.

### Example 3: Set the location of a user
```
PS C:\> Set-MsolUser -UserPrincipalName "davidchew@contoso.com" -UsageLocation "CA"
```

This command sets the location country of a user.
The country must be a two-letter ISO code.
This can be set for synced users as well as managed users.

### Example 4: Set the preferred data location
```
PS C:\> Set-MsolUser -UserPrincipalName "davidchew@contoso.com" -PreferredDataLocation "EUR"
```

This command sets the preferred data location property of a user whose user principal name is davidchew@contoso.com to EUR.

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
Default value: None
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
Specifies the country or region of the user.

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

### -ObjectId
Specifies the unique object ID of the user.

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
Specifies the location of the office of the user.

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
Default value: None
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
Default value: None
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
Specifies the user ID of the user.

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

## NOTES

## RELATED LINKS
[Get-MsolUser](./Get-MsolUser.md)

[New-MsolUser](./New-MsolUser.md)

[Remove-MsolUser](./Remove-MsolUser.md)

[Restore-MsolUser](./Restore-MsolUser.md)

[Set-MsolUserLicense](./Set-MsolUserLicense.md)

[Set-MsolUserPassword](./Set-MsolUserPassword.md)

[Set-MsolUserPrincipalName](./Set-MsolUserPrincipalName.md)
