---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 7428E3E3-B66F-4EBF-9566-B5B2C9BC5DE1
---

# Set-MsolDomainAuthentication

## SYNOPSIS
Changes the authentication type of the domain.

## SYNTAX

```
Set-MsolDomainAuthentication -DomainName <String> -Authentication <DomainAuthenticationType>
 [-SigningCertificate <String>] [-NextSigningCertificate <String>] [-LogOffUri <String>]
 [-PassiveLogOnUri <String>] [-ActiveLogOnUri <String>] [-IssuerUri <String>] [-FederationBrandName <String>]
 [-MetadataExchangeUri <String>] [-PreferredAuthenticationProtocol <AuthenticationProtocol>]
 [-SupportsMfa <Boolean>] [-DefaultInteractiveAuthenticationMethod <String>]
 [-OpenIdConnectDiscoveryEndpoint <String>] [-SigningCertificateUpdateStatus <SigningCertificateUpdateStatus>]
 [-PromptLoginBehavior <PromptLoginBehavior>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolDomainAuthentication cmdlet is used to change the domain authentication between standard identity and single-sign on.
This cmdlet will only update the settings in Microsoft Azure Active Directory; typically the Convert-MsolDomainToStandard or Convert-MsolDomainToFederated should be used instead.

## PARAMETERS

### -ActiveLogOnUri
A URL that specifies the end point used by active clients when authenticating with domains set up for single sign-on (also known as identity federation) in Microsoft Azure Active Directory.

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

### -Authentication
The authentication type (managed/federated) of the domain.
All users created on this domain will have this authentication type.

```yaml
Type: DomainAuthenticationType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainName
The fully qualified domain name (FQDN) to update.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FederationBrandName
The name of the string value shown to users when signing in to Microsoft Azure Active Directory services.
We recommend that customers user something that is familiar to them, such as "Contoso, Inc."

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

### -IssuerUri
The unique identifier of the domain in the Microsoft Azure Active Directory identity platform derived from the federation server.

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

### -LogOffUri
The URL clients are redirected to when they sign out of Microsoft Azure Active Directory services.

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

### -MetadataExchangeUri
The URL that specifies the metadata exchange end point used for authentication from rich client applications such as Lync Online.

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

### -NextSigningCertificate
The next token signing certificate that will be used to sign tokens when the primary signing certificate expires.

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

### -PassiveLogOnUri
The URL that web-based clients will be directed to when signing in to Microsoft Azure Active Directory services.

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

### -SigningCertificate
The current certificate used to sign tokens passed to the Microsoft Azure Active Directory Identity platform.

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

### -SupportsMfa
Indicates whether the IDP STS supports MFA.

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

### -DefaultInteractiveAuthenticationMethod
Indicates the default authentication method that should be used when an application requires the user to have interactive login.

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

### -OpenIdConnectDiscoveryEndpoint
The OpenID Connect Discovery Endpoint of the federated IDP STS.

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

### -PreferredAuthenticationProtocol


```yaml
Type: AuthenticationProtocol
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromptLoginBehavior


```yaml
Type: PromptLoginBehavior
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SigningCertificateUpdateStatus


```yaml
Type: SigningCertificateUpdateStatus
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


