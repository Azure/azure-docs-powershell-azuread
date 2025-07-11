---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Set-AzureADApplication

## SYNOPSIS
Updates an application.

## SYNTAX

```
Set-AzureADApplication -ObjectId <String>
 [-AddIns <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AddIn]>]
 [-AllowGuestsSignIn <Boolean>] [-AllowPassthroughUsers <Boolean>] [-AppLogoUrl <String>]
 [-AppRoles <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AppRole]>]
 [-AvailableToOtherTenants <Boolean>] [-DisplayName <String>] [-ErrorUrl <String>]
 [-GroupMembershipClaims <String>] [-Homepage <String>]
 [-IdentifierUris <System.Collections.Generic.List`1[System.String]>] [-InformationalUrls <InformationalUrl>]
 [-IsDeviceOnlyAuthSupported <Boolean>] [-IsDisabled <Boolean>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]>]
 [-KnownClientApplications <System.Collections.Generic.List`1[System.String]>] [-LogoutUrl <String>]
 [-Oauth2AllowImplicitFlow <Boolean>] [-Oauth2AllowUrlPathMatching <Boolean>]
 [-Oauth2Permissions <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.OAuth2Permission]>]
 [-Oauth2RequirePostResponse <Boolean>] [-OrgRestrictions <System.Collections.Generic.List`1[System.String]>]
 [-OptionalClaims <OptionalClaims>] [-ParentalControlSettings <ParentalControlSettings>]
 [-PasswordCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PasswordCredential]>]
 [-PreAuthorizedApplications <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PreAuthorizedApplication]>]
 [-PublicClient <Boolean>] [-PublisherDomain <String>] [-RecordConsentConditions <String>]
 [-ReplyUrls <System.Collections.Generic.List`1[System.String]>]
 [-RequiredResourceAccess <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.RequiredResourceAccess]>]
 [-SamlMetadataUrl <String>] [-SignInAudience <String>] [-WwwHomepage <String>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Update an application
```
PS C:\>Set-AzureADApplication -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -DisplayName "New Name"
```

This command updates the specified application.

## PARAMETERS

### -AddIns
Defines custom behavior that a consuming service can use to call an app in specific contexts.
For example, applications that can render file streams may set the addIns property for its "FileHandler" functionality.
This will let services like Office 365 call the application in the context of a document the user is working on.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AddIn]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppRoles
The collection of application roles that an application may declare.
These roles can be assigned to users, groups or service principals.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AppRole]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableToOtherTenants
True if the application is shared with other tenants; otherwise, false.

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

### -DisplayName
Specifies the display name.

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

### -ErrorUrl
Specifies an error URL.

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

### -GroupMembershipClaims
A bitmask that configures the "groups" claim issued in a user or OAuth 2.0 access token that the application expects.
The bitmask values are: 0: None, 1: Security groups and Azure AD roles, 2: Reserved, and 4: Reserved.
Setting the bitmask to 7 will get all of the security groups, distribution groups, and Azure AD directory roles that the signed-in user is a member of.

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

### -Homepage
Specifies the home page.

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

### -IdentifierUris
Specifies identifier URIs.

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

### -KeyCredentials
Specifies key credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KnownClientApplications
Specifies known client applications.

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

### -LogoutUrl
Specifies the logout URL.

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

### -Oauth2AllowImplicitFlow
Specifies whether this web application can request OAuth2.0 implicit flow tokens.
The default is false.

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

### -Oauth2AllowUrlPathMatching
Specifies whether, as part of OAuth 2.0 token requests, Azure AD will allow path matching of the redirect URI against the application's replyUrls.
The default is false.

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

### -Oauth2Permissions
The collection of OAuth 2.0 permission scopes that the web API (resource) application exposes to client applications.
These permission scopes may be granted to client applications during consent.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.OAuth2Permission]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID of an application in Azure AD.

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

### -PasswordCredentials
Specifies password credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PasswordCredential]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicClient
Specifies whether this application is a public client (such as an installed application running on a mobile device).
Default is false.

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

### -RecordConsentConditions
Do not use.
May be removed in future versions

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

### -ReplyUrls
Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.

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

### -RequiredResourceAccess
@{Text=}

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.RequiredResourceAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SamlMetadataUrl
@{Text=}

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

### -Oauth2RequirePostResponse
{{Fill Oauth2RequirePostResponse Description}}

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

### -AllowGuestsSignIn
{{ Fill AllowGuestsSignIn Description }}

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

### -AllowPassthroughUsers
{{ Fill AllowPassthroughUsers Description }}

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

### -AppLogoUrl
{{ Fill AppLogoUrl Description }}

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

### -InformationalUrls
{{ Fill InformationalUrls Description }}

```yaml
Type: InformationalUrl
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDeviceOnlyAuthSupported
{{ Fill IsDeviceOnlyAuthSupported Description }}

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

### -IsDisabled
{{ Fill IsDisabled Description }}

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

### -OptionalClaims
{{ Fill OptionalClaims Description }}

```yaml
Type: OptionalClaims
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrgRestrictions
{{ Fill OrgRestrictions Description }}

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

### -ParentalControlSettings
{{ Fill ParentalControlSettings Description }}

```yaml
Type: ParentalControlSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreAuthorizedApplications
{{ Fill PreAuthorizedApplications Description }}

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PreAuthorizedApplication]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublisherDomain
{{ Fill PublisherDomain Description }}

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

### -SignInAudience
{{ Fill SignInAudience Description }}

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

### -WwwHomepage
{{ Fill WwwHomepage Description }}

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

[Get-AzureADApplication]()

[New-AzureADApplication]()

[Remove-AzureADApplication]()
