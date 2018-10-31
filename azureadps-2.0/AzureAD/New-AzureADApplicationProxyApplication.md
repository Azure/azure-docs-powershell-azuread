---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureADApplicationProxyApplication

## SYNOPSIS
The New-AzureADApplicationProxyApplication cmdlet creates a new application configured for Application Proxy in Azure Active Directory. 

## SYNTAX

```
New-AzureADApplicationProxyApplication -DisplayName <String> -ExternalUrl <String> -InternalUrl <String>
 [-ExternalAuthenticationType <ExternalAuthenticationTypeEnum>] [-IsTranslateHostHeaderEnabled <Boolean>]
 [-IsTranslateLinksInBodyEnabled <Boolean>] [-ApplicationServerTimeout <ApplicationServerTimeoutEnum>]
 [-ConnectorGroupId <String>]
```

## DESCRIPTION
The New-AzureADApplicationProxyApplication cmdlet creates a new application configured for Application Proxy in Azure Active Directory. To ensure this application is usable, please also make sure you assign users and configure SSO if needed. Note that without specifying a ConnectorGroupId, this application by default will use the �Default� connector group in your tenant.

## EXAMPLES

### Example 1
```
PS C:\> New-AzureADApplicationProxyApplication -DisplayName "Finance Tracker" -ExternalUrl "https://finance-awcycles.msappproxy.net/" -InternalUrl "http://finance/" 


ExternalAuthenticationType               : AadPreAuthentication
ApplicationServerTimeout                 : Default
ExternalUrl                              : https://finance-awcycles.msappproxy.net/
InternalUrl                              : http://finance/
IsTranslateHostHeaderEnabled             : True
IsTranslateLinksInBodyEnabled            : False
IsOnPremPublishingEnabled                : True
VerifiedCustomDomainCertificatesMetadata : 
VerifiedCustomDomainKeyCredential        : 
VerifiedCustomDomainPasswordCredential   : 
SingleSignOnSettings                     : 
```
Example 1: Creating a new application with only the basic required settings, and the default domain for applications.

### Example 2
```
PS C:\> New-AzureADApplicationProxyApplication -DisplayName "HR Resources" -ExternalUrl "https://hr.adventure-works.com/" -InternalUrl "http://hr.adventure-works.com/" -ApplicationServerTimeout Long 


ExternalAuthenticationType               : AadPreAuthentication
ApplicationServerTimeout                 : Long
ExternalUrl                              : https://hr.adventure-works.com/
InternalUrl                              : http://hr.adventure-works.com/
IsTranslateHostHeaderEnabled             : True
IsTranslateLinksInBodyEnabled            : False
IsOnPremPublishingEnabled                : True
VerifiedCustomDomainCertificatesMetadata : class OnPremisesPublishingVerifiedCustomDomainCertificatesMetadataObject {
                                             Thumbprint: [XXXXX]
                                             SubjectName: [XXXXX]
                                             Issuer: 
                                             IssueDate: 11/9/2017 5:54:29
                                             ExpiryDate: 11/9/2019 5:54:29
                                           }

VerifiedCustomDomainKeyCredential        : 
VerifiedCustomDomainPasswordCredential   : 
SingleSignOnSettings                     :  
```
Example 2: Creating a new application that uses a custom domain and sets several optional flags.

## PARAMETERS

### -ApplicationServerTimeout
Set this value to Long only if your application is slow to authenticate and connect. 

```yaml
Type: ApplicationServerTimeoutEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Default, Long

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

### -DisplayName
The displayname of the new Application

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

### -ExternalAuthenticationType
How Application Proxy verifies users before giving them access to your application. 
AadPreAuthentication: Application Proxy redirects users to sign in with Azure AD, which authenticates their permissions for the directory and application. We recommend keeping this option as the default, so that you can take advantage of Azure AD security features like conditional access and Multi-Factor Authentication.
Passthru: Users don't have to authenticate against Azure Active Directory to access the application. You can still set up authentication requirements on the backend.

```yaml
Type: ExternalAuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: AadPreAuthentication, Passthru

Required: False
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

Required: True
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

Required: True
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

## INPUTS

### System.String
System.Nullable`1[[Microsoft.Open.MSGraph.Model.ApplicationProxyApplicationObject+ExternalAuthenticationTypeEnum, Microsoft.Open.MS.GraphBeta.Client, Version=2.0.0.0, Culture=neutral, PublicKeyToken=null]]
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Open.MSGraph.Model.ApplicationProxyApplicationObject+ApplicationServerTimeoutEnum, Microsoft.Open.MS.GraphBeta.Client, Version=2.0.0.0, Culture=neutral, PublicKeyToken=null]]


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

