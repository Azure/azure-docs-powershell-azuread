---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 8DC24A62-AD0A-452B-BACF-28B9BEC922FC
---

# Confirm-MsolDomain

## SYNOPSIS
Verifies a custom domain.

## SYNTAX

```
Confirm-MsolDomain -DomainName <String> [-SigningCertificate <String>] [-NextSigningCertificate <String>]
 [-LogOffUri <String>] [-PassiveLogOnUri <String>] [-ActiveLogOnUri <String>] [-IssuerUri <String>]
 [-FederationBrandName <String>] [-MetadataExchangeUri <String>]
 [-PreferredAuthenticationProtocol <AuthenticationProtocol>] [-SupportsMfa <Boolean>]
 [-DefaultInteractiveAuthenticationMethod <String>] [-OpenIdConnectDiscoveryEndpoint <String>]
 [-SigningCertificateUpdateStatus <SigningCertificateUpdateStatus>]
 [-PromptLoginBehavior <PromptLoginBehavior>] [-ForceTakeover <ForceTakeoverOption>] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to confirm ownership of a domain.
In order to confirm ownership, a custom TXT or MX DNS record must be added for the domain.
The domain must first be added using the New-MsolDomain cmdlet, and then the Get-MsolDomainVerificationDNS cmdlet should be called to retrieve the details of the DNS record that must be set.

        Note that there may be a delay (15-60 minutes) between when the DNS update is made and when the cmdlet is able to verify.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Confirm-MsolDomain -DomainName contoso.com

          None
```

Description

-----------

This command attempts to verify the domain contoso.com. 
In order for domain verification to succeed, the appropriate DNS records must first be set up. 
The list of DNS records to set up can be retrieved using the Get-MsolDomainVerificationDns cmdlet.

## PARAMETERS

### -ActiveLogOnUri
A URL that specifies the end point used by active clients when authenticating with domains set up for single sign-on (also known as identity federation) with Microsoft Azure Active Directory.

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
The fully qualified domain name to verify.

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
The name of the string value shown to users when signing in to Microsoft Azure Active Directory Services.
It is recommended that customers use something that is familiar to users, such as "Contoso Inc."

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
The unique identifier of the domain in the Microsoft Azure Active Directory identity platform that is derived from the federation server.

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
The URL clients are redirected to when they sign out of Microsoft Azure Active Directory Services.

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
The URL that web based clients will be directed to when signing in to Microsoft Azure Active Directory Services.

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

### -ForceTakeover


```yaml
Type: ForceTakeoverOption
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


