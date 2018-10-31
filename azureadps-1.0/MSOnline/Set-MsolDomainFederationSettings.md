---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0E9207E0-65AB-4965-B282-C8FE5E13F1E4
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolDomainFederationSettings

## SYNOPSIS
Updates settings for a federated domain.

## SYNTAX

```
Set-MsolDomainFederationSettings -DomainName <String> [-SigningCertificate <String>]
 [-NextSigningCertificate <String>] [-LogOffUri <String>] [-PassiveLogOnUri <String>]
 [-ActiveLogOnUri <String>] [-IssuerUri <String>] [-FederationBrandName <String>]
 [-MetadataExchangeUri <String>] [-PreferredAuthenticationProtocol <AuthenticationProtocol>]
 [-SupportsMfa <Boolean>] [-DefaultInteractiveAuthenticationMethod <String>]
 [-OpenIdConnectDiscoveryEndpoint <String>] [-SigningCertificateUpdateStatus <SigningCertificateUpdateStatus>]
 [-PromptLoginBehavior <PromptLoginBehavior>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolDomainFederationSettings** cmdlet is used to update the settings of a single sign-on domain.
Single sign-on is also known as identity federation.

## PARAMETERS

### -ActiveLogOnUri
Specifies the URL of the end point used by active clients when authenticating with domains set up for single sign-on in Azure Active Directory.

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
Specifies the name of the string value shown to users when signing in to Azure Active Directory.
We recommend that you use something that is familiar to users, like your company name, such as Contoso Inc.

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
Specifies the URI of the domain in the Azure Active Directory Identity platform derived from the federation server.

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
Specifies the URL clients are redirected to when they sign out of Azure Active Directory services.

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
Specifies the next token signing certificate that to use to sign tokens when the primary signing certificate expires.

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
Specifies the prompt login behavior.

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
[Get-MsolDomainFederationSettings](./Get-MsolDomainFederationSettings.md)
