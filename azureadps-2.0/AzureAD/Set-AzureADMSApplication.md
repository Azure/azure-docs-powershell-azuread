---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSApplication

## SYNOPSIS
Updates the properties of an application object.

## SYNTAX

```
Set-AzureADMSApplication -ObjectId <String>
 [-AddIns <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AddIn]>] [-Api <ApiApplication>]
 [-AppRoles <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AppRole]>]
 [-GroupMembershipClaims <String>] [-IsDeviceOnlyAuthSupported <Boolean>] [-IsFallbackPublicClient <Boolean>]
 [-IdentifierUris <System.Collections.Generic.List`1[System.String]>] [-DisplayName <String>]
 [-InformationalUrl <InformationalUrl>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.KeyCredential]>]
 [-OptionalClaims <OptionalClaims>] [-ParentalControlSettings <ParentalControlSettings>]
 [-PasswordCredentials <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PasswordCredential]>]
 [-PublicClient <PublicClientApplication>]
 [-RequiredResourceAccess <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RequiredResourceAccess]>]
 [-SignInAudience <String>] [-Tags <System.Collections.Generic.List`1[System.String]>]
 [-TokenEncryptionKeyId <String>] [-Web <WebApplication>] [<CommonParameters>]
```

## DESCRIPTION
Updates the properties of an application object.

## EXAMPLES

### Example 1: Update an application
```
PS C:\>Set-AzureADMSApplication -ObjectId fcd37fb8-449c-45af-92fc-5448c671fd30 `
          -DisplayName "my name" `
          -AddIns @{ Type = "mytype"; Properties = [PSCustomObject]@{ Key = "key"; Value = "value" } } `
          -Api @{ AcceptMappedClaims = $true } `
          -AppRoles @{ Id = "21111111-1111-1111-1111-111111111111"; DisplayName = "role"; AllowedMemberTypes = "User"; Description = "mydescription"; Value = "myvalue" } `
          -InformationalUrl @{ SupportUrl = "https://mynewapp.contoso.com/support.html" } `
          -IsDeviceOnlyAuthSupported $false `
          -IsFallbackPublicClient $false `
          -KeyCredentials @{ KeyId = "41111111-1111-1111-1111-111111111111"; Usage = "Encrypt"; Key = [System.IO.File]::ReadAllBytes("file.cer"); Type = "AsymmetricX509Cert" } `
          -OptionalClaims @{ IdToken = [PSCustomObject]@{ Name = "claimName"; Source = "claimSource" } } `
          -ParentalControlSettings @{ LegalAgeGroupRule = "Block" } `
          -PublicClient @{ RedirectUris = "https://mynewapp.contoso.com/" } `
          -RequiredResourceAccess @{ ResourceAppId = "31111111-1111-1111-1111-111111111111"; ResourceAccess = [PSCustomObject]@{ Type = "Scope" } } `
          -SignInAudience AzureADandPersonalMicrosoftAccount `
          -Tags "mytag" `
          -TokenEncryptionKeyId "41111111-1111-1111-1111-111111111111" `
          -Web @{ LogoutUrl = "https://mynewapp.contoso.com/logout.html" } `
          -GroupMembershipClaims "SecurityGroup" `
          -IdentifierUris "https://mynewapp.contoso.com"`
          -PasswordCredentials {passwordcredentials}
```

This command updates the specified application.

## PARAMETERS

### -AddIns
Defines custom behavior that a consuming service can use to call an app in specific contexts.
For example, applications that can render file streams may set the addIns property for its "FileHandler" functionality.
This will let services like Office 365 call the application in the context of a document the user is working on.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AddIn]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Api
Specifies settings for an application that implements a web API.

```yaml
Type: ApiApplication
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
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AppRole]
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

### -GroupMembershipClaims
Configures the groups claim issued in a user or OAuth 2.0 access token that the application expects.

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

### -InformationalUrl
Basic profile information of the application such as app's marketing, support, terms of service and privacy statement URLs.
The terms of service and privacy statement are surfaced to users through the user consent experience.

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
Specifies if the application supports authentication using a device token.

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

### -IsFallbackPublicClient
Specifies the fallback application type as public client, such as an installed application running on a mobile device.
The default value is false which means the fallback application type is confidential client such as web app.
There are certain scenarios where Azure AD cannot determine the client application type (e.g.
ROPC flow where it is configured without specifying a redirect URI).
In those cases Azure AD will interpret the application type based on the value of this property.

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

### -KeyCredentials
Specifies key credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.KeyCredential]
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

### -OptionalClaims
Application developers can configure optional claims in their Azure AD apps to specify which claims they want in tokens sent to their application by the Microsoft security token service.

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

### -ParentalControlSettings
Specifies parental control settings for an application.

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

### -PasswordCredentials
The collection of password credentials associated with the application

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PasswordCredential]
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

Specifies whether this application is a public client (such as an installed application running on a mobile device).
Default is false.

```yaml
Type: PublicClientApplication
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
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RequiredResourceAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInAudience
Specifies what Microsoft accounts are supported for the current application.

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

### -Tags
Custom strings that can be used to categorize and identify the application.

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

### -TokenEncryptionKeyId
Specifies the keyId of a public key from the keyCredentials collection.
When configured, Azure AD encrypts all the tokens it emits by using the key this property points to.
The application code that receives the encrypted token must use the matching private key to decrypt the token before it can be used for the signed-in user.

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

### -Web
Specifies settings for a web application.

```yaml
Type: WebApplication
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

### Boolean
### Microsoft.Open.MSGraph.Model.ApiApplication
### Microsoft.Open.MSGraph.Model.InformationalUrl
### Microsoft.Open.MSGraph.Model.OptionalClaims
### Microsoft.Open.MSGraph.Model.ParentalControlSettings
### Microsoft.Open.MSGraph.Model.PublicClientApplication
### Microsoft.Open.MSGraph.Model.WebApplication
### string
### System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AddIn]
### System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AppRole]
### System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.KeyCredential]
### System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.PasswordCredential]
### System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.RequiredResourceAccess]
### System.Collections.Generic.List`1[System.String]
### System.Nullable`1[System.Boolean]
## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADMSApplication]()

[New-AzureADMSApplication]()

[Remove-AzureADMSApplication]()

