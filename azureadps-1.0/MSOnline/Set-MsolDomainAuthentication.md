---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 7428E3E3-B66F-4EBF-9566-B5B2C9BC5DE1
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
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
The **Set-MsolDomainAuthentication** cmdlet changes the domain authentication between standard identity and single-sign on.
This cmdlet update only the settings in Azure Active Directory.
Typically, the [Convert-MsolDomainToStandard](./Convert-MsolDomainToStandard.md) or [Convert-MsolDomainToFederated](./Convert-MsolDomainToFederated.md) cmdlet should be used instead.

## PARAMETERS

### -ActiveLogOnUri
Specifies the URL of the end point used by active clients when authenticating with domains set up for single sign-on in Azure Active Directory.
Single sign-on is also known as identity federation.

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
Specifies the authentication type of the domain.
Valid values are: managed and federated.
All users created on this domain have this authentication type.

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
Specifies the fully qualified domain name (FQDN) to update.

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
Specifies the name of the string value shown to users when signing in to Azure Active Directory services.
We recommend that customers use something that is familiar to them, like their company name, such as Contoso, Inc.

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
Specifies the URI of the domain in the Azure Active Directory identity platform derived from the federation server.

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
Specifies the URL that clients are redirected to when they sign out of Azure Active Directory services.

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
Specifies the URL of the metadata exchange end point used for authentication from rich client applications such as Lync Online.

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
Specifies the next token signing certificate that is used to sign tokens when the primary signing certificate expires.

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
Specifies the URL that web-based clients are directed to when signing in to Azure Active Directory services.

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
Specifies the current certificate used to sign tokens passed to the Azure Active Directory Identity platform.

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
Specifies the default authentication method that should be used when an application requires the user to have interactive login.

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
Specifies the OpenID Connect Discovery Endpoint of the federated IDP STS.

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
Specifies the preferred authentication protocol.

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
Specifies the prompt log-in behavior.

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
Specifies the update status of the signing certificate.

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
[Convert-MsolDomainToFederated](./Convert-MsolDomainToFederated.md)

[Convert-MsolDomainToStandard](./Convert-MsolDomainToStandard.md)
