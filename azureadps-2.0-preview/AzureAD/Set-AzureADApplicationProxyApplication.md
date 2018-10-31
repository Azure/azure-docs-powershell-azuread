---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationProxyApplication

## SYNOPSIS
The Set-AzureADApplicationProxyApplication allows you to modify and set configurations for an application in Azure Active Directory configured to use ApplicationProxy. 

## SYNTAX

```
Set-AzureADApplicationProxyApplication -ObjectId <String> [-ExternalUrl <String>] [-InternalUrl <String>]
 [-ExternalAuthenticationType <ExternalAuthenticationTypeEnum>] [-IsTranslateHostHeaderEnabled <Boolean>]
 [-IsTranslateLinksInBodyEnabled <Boolean>] [-ApplicationServerTimeout <ApplicationServerTimeoutEnum>]
 [-ConnectorGroupId <String>]
```

## DESCRIPTION
The Set-AzureADApplicationProxyApplication allows you to modify and set additional settings for an application in Azure Active Directory configured to use ApplicationProxy. 

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADApplicationProxyApplication -ObjectId 257098d1-f8dd-4efb-88a2-1c92d3654f10 -IsTranslateLinksInBodyEnabled $true


ExternalAuthenticationType               : AadPreAuthentication
ApplicationServerTimeout                 : Default
ExternalUrl                              : https://finance-awcycles.msappproxy.net/
InternalUrl                              : http://finance/
IsTranslateHostHeaderEnabled             : True
IsTranslateLinksInBodyEnabled            : True
IsOnPremPublishingEnabled                : True
VerifiedCustomDomainCertificatesMetadata : 
VerifiedCustomDomainKeyCredential        : 
VerifiedCustomDomainPasswordCredential   : 
SingleSignOnSettings                     :  
```

Example 1: Add the link translation feature to an application

## PARAMETERS

### -ObjectId
Specifies a unique application ID of an application in Azure Active Directory. This can be found using the Get-AzureADApplication command.

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

### -ExternalUrl
The address your users will go to in order to access the app from outside your network. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InternalUrl
The URL that you use to access the application from inside your private network. You can provide a specific path on the backend server to publish, while the rest of the server is unpublished. In this way, you can publish different sites on the same server as different apps, and give each one its own name and access rules. If you publish a path, make sure that it includes all the necessary images, scripts, and style sheets for your application. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExternalAuthenticationType
How Application Proxy verifies users before giving them access to your application. 
AadPreAuth: Application Proxy redirects users to sign in with Azure AD, which authenticates their permissions for the directory and application. We recommend keeping this option as the default, so that you can take advantage of Azure AD security features like conditional access and Multi-Factor Authentication.
Passthru: Users don't have to authenticate against Azure Active Directory to access the application. You can still set up authentication requirements on the backend.

```yaml
Type: ExternalAuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -IsTranslateHostHeaderEnabled
If set to true, translates urls in headers. Keep this value true unless your application required the original host header in the authentication request.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -IsTranslateLinksInBodyEnabled
If set to true, translates urls in body. Keep this value as No unless you have hardcoded HTML links to other on-premises applications, and don't use custom domains.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ApplicationServerTimeout
Specifies the backend server timeout type. Set this value to Long only if your application is slow to authenticate and connect. 

```yaml
Type: ApplicationServerTimeoutEnum
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ConnectorGroupId
Provide the Id of the Connector group you would like assigned to this application. You can find this value by using the Get-AzureADApplicationProxyConnectorGroup command.
Connectors process the remote access to your application, and connector groups help you organize connectors and apps by region, network, or purpose. If you don't have any connector groups created yet, your app is assigned to Default.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

