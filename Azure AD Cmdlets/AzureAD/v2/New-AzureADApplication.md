---
external help file: azuread.help.xml
online version: https://docs.microsoft.com/en-us/powershell/azuread/v2/new-azureadapplication
schema: 2.0.0
---

# New-AzureADApplication

## SYNOPSIS
Create a new application in Azure Active Directory

## SYNTAX

```
New-AzureADApplication [-AppRoles <List`1[AppRole]>] [-AvailableToOtherTenants <Nullable`1[Boolean]>]
 -DisplayName <String> [-ErrorUrl <String>] [-Homepage <String>] [-IdentifierUris <List`1[String]>]
 [-KeyCredentials <List`1[KeyCredential]>] [-KnownClientApplications <List`1[String]>] [-LogoutUrl <String>]
 [-MainLogo <Byte[]>] [-Oauth2AllowImplicitFlow <Nullable`1[Boolean]>]
 [-Oauth2AllowUrlPathMatching <Nullable`1[Boolean]>] [-Oauth2Permissions <List`1[OAuth2Permission]>]
 [-OAuth2RequiredPostResponse <Nullable`1[Boolean]>] [-PasswordCredentials <List`1[PasswordCredential]>]
 [-PublicClient <Nullable`1[Boolean]>] [-ReplyUrls <List`1[String]>]
 [-RequiredResourceAccess <List`1[RequiredResourceAccess]>] [-SamlMetadataUrl <String>]
```

## DESCRIPTION

## EXAMPLES

### Create a new application
```
New-AzureADApplication -DisplayName "My new application"  -IdentifierUris "http://mynewapp.contoso.com"

Output:


ObjectId                             AppId                                DisplayName 
--------                             -----                                ----------- 
acd10942-5747-4385-8824-4c5d5fa904f9 b5fecfab-0ea2-4fd1-8570-b2c41b3d5149 My new application
```

## PARAMETERS

### -AppRoles
The collection of application roles that an application may declare.
These roles can be assigned to users, groups or service principals

```yaml
Type: List`1[AppRole]
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
Type: Nullable`1[Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
The display name of the new application

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorUrl
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

### -Homepage
The URL to the application's home page

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
User-defined URI(s) that uniquely identify a Web application within its Azure AD tenant, or within a verified custom domain (see "Domains" tab in the Azure classic portal) if the application is multi-tenant. 

The first element is populated from the Web application's "APP ID URIâ€ field if updated via the Azure classic portal (or respective Azure AD PowerShell cmdlet parameter).
Additional URIs can be added via the application manifest; see Understanding the Azure AD Application Manifest for details.
This collection is also used to populate the Web application's servicePrincipalNames collection. 

Notes: not nullable, the any operator is required for filter expressions on multi-valued properties;

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

### -KeyCredentials
The collection of key credentials associated with the application

```yaml
Type: List`1[KeyCredential]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KnownClientApplications
Client applications that are tied to this resource application.
Consent to any of the known client applications will result in implicit consent to the resource application through a combined consent dialog (showing the OAuth permission scopes required by the client and the resource).

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

### -LogoutUrl
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

### -MainLogo
The main logo for this application

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

### -Oauth2AllowImplicitFlow
Specifies whether this web application can request OAuth2.0 implicit flow tokens.
The default is false.

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

### -Oauth2AllowUrlPathMatching
Specifies whether, as part of OAuth 2.0 token requests, Azure AD will allow path matching of the redirect URI against the application's replyUrls.
The default is false.

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

### -Oauth2Permissions
The collection of OAuth 2.0 permission scopes that the web API (resource) application exposes to client applications.
These permission scopes may be granted to client applications during consent.

```yaml
Type: List`1[OAuth2Permission]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OAuth2RequiredPostResponse
Specifies whether, as part of OAuth 2.0 token requests, Azure AD will allow POST requests, as opposed to GET requests.
The default is false, which specifies that only GET requests will be allowed.

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

### -PasswordCredentials
The collection of password credentials associated with the application.

```yaml
Type: List`1[PasswordCredential]
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
Type: Nullable`1[Boolean]
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
Type: List`1[String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequiredResourceAccess
Specifies resources that this application requires access to and the set of OAuth permission scopes and application roles that it needs under each of those resources.
This pre-configuration of required resource access drives the consent experience.

```yaml
Type: List`1[RequiredResourceAccess]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SamlMetadataUrl
The URL to the SAML metadata for the application.

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

[https://docs.microsoft.com/en-us/powershell/azuread/v2/new-azureadapplication](https://docs.microsoft.com/en-us/powershell/azuread/v2/new-azureadapplication)

