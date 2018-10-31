---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationProxyApplicationSingleSignOn

## SYNOPSIS
The Set-AzureADApplicationProxyApplicationSingleSignOn cmdlet allows you to set and modify single sign-on (SSO) settings for an application configured for Application Proxy in Azure Active Directory. 
## SYNTAX

```
Set-AzureADApplicationProxyApplicationSingleSignOn -ObjectId <String> -SingleSignOnMode <SingleSignOnModeEnum>
 [-KerberosInternalApplicationServicePrincipalName <String>]
 [-KerberosDelegatedLoginIdentity <KerberosSignOnMappingAttributeTypeEnum>]
```

## DESCRIPTION
The Set-AzureADApplicationProxyApplicationSingleSignOn cmdlet allows you to set and modify single sign-on (SSO) settings for an application configured for Application Proxy in Azure Active Directory. This is limited to setting No SSO, Kerberos Constrained Delegation (for applications using Integrated Windows Authentication), and Header-based SSO.

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADApplicationProxyApplicationSingleSignOn -ObjectId 4eba5342-8d17-4eac-a1f6-62a0de26311e -SingleSignOnMode OnPremisesKerberos -KerberosInternalApplicationServicePrincipalName "http/www.adventure-works.com" -KerberosDelegatedLoginIdentity OnPremisesUserPrincipalName
```
Example 1: Assign an application to use Kerberos Constrained Delegation, and specify required parameters. 

### Example 2
```
PS C:\> Set-AzureADApplicationProxyApplicationSingleSignOn -ObjectId 4eba5342-8d17-4eac-a1f6-62a0de26311e -SingleSignOnMode None
```
Example 2: Remove SSO from an application

## PARAMETERS

### -KerberosDelegatedLoginIdentity
The identity that the Connector can use on behalf of your users to authenticate. 

```yaml
Type: KerberosSignOnMappingAttributeTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: UserPrincipalName, OnPremisesUserPrincipalName, UserPrincipalUsername, OnPremisesUserPrincipalUsername, OnPremisesSAMAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -KerberosInternalApplicationServicePrincipalName
The internal application SPN of the application server. This SPN needs to be in the list of services to which the Connector can present delegated credentials.

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

### -ObjectId
The unique application Id of the application that needs different SSO settings. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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

### -SingleSignOnMode
Choose the type of SSO you would like the application to use. Please note that only three SSO settings are supported in powershell, for more options, please use the Azure Portal.

```yaml
Type: SingleSignOnModeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, OnPremisesKerberos, HeaderBased

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.String
System.Nullable`1[[Microsoft.Open.MSGraph.Model.OnPremisesPublishingSingleSignOnObject+SingleSignOnModeEnum, Microsoft.Open.MS.GraphBeta.Client, Version=2.0.0.0, Culture=neutral, PublicKeyToken=null]]
System.Nullable`1[[Microsoft.Open.MSGraph.Model.OnPremisesPublishingKerberosSignOnSettingsObject+KerberosSignOnMappingAttributeTypeEnum, Microsoft.Open.MS.GraphBeta.Client, Version=2.0.0.0, Culture=neutral, PublicKeyToken=null]]


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

