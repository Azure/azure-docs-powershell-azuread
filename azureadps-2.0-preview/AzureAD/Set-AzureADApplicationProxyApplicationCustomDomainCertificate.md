---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationProxyApplicationCustomDomainCertificate

## SYNOPSIS
The Set-AzureADApplicationProxyApplicationCustomDomainCertificate cmdlet assigns a certificate to an application configured for Application Proxy in Azure Active Directory (AD). This will upload the certificate and allow the application to use Custom Domains. 

## SYNTAX

```
Set-AzureADApplicationProxyApplicationCustomDomainCertificate -ObjectId <String> -PfxFilePath <String>
 -Password <SecureString>
```

## DESCRIPTION
The Set-AzureADApplicationProxyApplicationCustomDomainCertificate cmdlet assigns a certificate to an application configured for Application Proxy in Azure Active Directory (AD). This will upload the certificate and allow the application to use Custom Domains. If you have one certificate that includes many of your applications, you only need to upload it with one application and it will also be assigned to the other relevant applications.

## EXAMPLES

### Example 1
```
PS C:\> $securePassword = Read-Host -AsSecureString
PS C:\> Set-AzureADApplicationProxyApplicationCustomDomainCertificate -ObjectId 4eba5342-8d17-4eac-a1f6-62a0de26311e -PfxFilePath "C:\Temp\Certificates\cert.pfx" -Password $securePassword 
```

Example 1: Assign a certificate to an application configured for Application Proxy

## PARAMETERS

### -ObjectId
The unique application Id for the application the certificate should be uploaded to. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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

### -Password
A secure string containing the password for the pfx certificate

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PfxFilePath
The file path for the pfx certificate for the custom domain

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
System.Security.SecureString


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

