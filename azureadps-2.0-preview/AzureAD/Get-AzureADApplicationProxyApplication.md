---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationProxyApplication

## SYNOPSIS
The Get-AzureADApplicationProxyApplication cmdlet retrieves an application configured for Application Proxy in Azure Active Directory. 

## SYNTAX

```
Get-AzureADApplicationProxyApplication -ObjectId <String>
```

## DESCRIPTION
The Get-AzureADApplicationProxyApplication cmdlet retrieves an application configured for Application Proxy in Azure Active Directory. 

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADApplicationProxyApplication -ObjectId 8d6c6684-6f8c-42e2-8914-32ed2adf9ccf


ExternalAuthenticationType               : AadPreAuthentication
ApplicationServerTimeout                 : Default
ExternalUrl                              : https://travel.cycles.adventure-works.com/
InternalUrl                              : https://awcyclesapps.adventure-works.com:3000/
IsTranslateHostHeaderEnabled             : False
IsTranslateLinksInBodyEnabled            : False
IsOnPremPublishingEnabled                : True
VerifiedCustomDomainCertificatesMetadata : class OnPremisesPublishingVerifiedCustomDomainCertificatesMetadataObject {
                                             Thumbprint:  [XXXXX]
                                             SubjectName: [XXXXX]
                                             Issuer: 
                                             IssueDate: 11/9/2017 5:54:29
                                             ExpiryDate: 11/9/2019 5:54:29
                                           }

VerifiedCustomDomainKeyCredential        : 
VerifiedCustomDomainPasswordCredential   : 
SingleSignOnSettings                     :  
```

## PARAMETERS

### -ObjectId
This is the unique application Id of the application. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

