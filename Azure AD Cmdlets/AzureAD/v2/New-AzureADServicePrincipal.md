---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADServicePrincipal

## SYNOPSIS
Create a new application in Azure Active Directory

## SYNTAX

```
New-AzureADServicePrincipal [-AccountEnabled <String>] -AppId <String>
 [-AppRoleAssignmentRequired <Nullable`1[Boolean]>] [-DisplayName <String>] [-ErrorUrl <String>]
 [-Homepage <String>] [-KeyCredentials <List`1[KeyCredential]>] [-LogoutUrl <String>]
 [-PasswordCredentials <List`1[PasswordCredential]>] [-PublisherName <String>] [-ReplyUrl <List`1[String]>]
 [-SamlMetadataUrl <String>] [-ServicePrincipalNames <List`1[String]>] [-Tags <List`1[String]>]
```

## DESCRIPTION

## EXAMPLES

### Create a new service principal
```
$MyApp = Get-AzureADApplication -top 1
$App = "My new application"
New-AzureADServicePrincipal -AccountEnabled true -AppId $MyApp.AppId -AppRoleAssignmentRequired $true -DisplayName $App
```

## PARAMETERS

### -AccountEnabled
true if the service principal account is enabled; otherwise, false.

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

### -AppId
The unique identifier for the associated application (its appId property).

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

### -AppRoleAssignmentRequired
Specifies whether an AppRoleAssignment to a user or group is required before Azure AD will issue a user or access token to the application.

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
The display name for the service principal.

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
The URL to the homepage of the associated application.

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

### -KeyCredentials
The collection of key credentials associated with the service principal.

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

### -PasswordCredentials
The collection of password credentials associated with the service principal.

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

### -PublisherName
The display name of the tenant in which the associated application is specified.

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

### -ReplyUrl
The URLs that user tokens are sent to for sign in with the associated application, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to for the associated application.

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

### -ServicePrincipalNames
Based on the identifierURIs collection, plus the application's appId property, these URIs are used to reference an application's service principal.
A client will use these to:

â€¢ populate requiredResourceAccess, via "Permissions to other applicationsâ€ in the Azure classic portal.
â€¢ specify a resource URI to acquire an access token, which is the URI returned in the â€œaudâ€ claim.

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

### -Tags
@{Text=}

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

