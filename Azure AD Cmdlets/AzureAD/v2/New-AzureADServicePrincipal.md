---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 7DC1958A-D7DE-44AF-A5B1-9C90ABF0B89A
online version: 
schema: 2.0.0
---

# New-AzureADServicePrincipal

## SYNOPSIS
Creates a service principal.

## SYNTAX

```
New-AzureADServicePrincipal [-AccountEnabled <String>]
 [-AlternativeNames <System.Collections.Generic.List`1[System.String]>] -AppId <String>
 [-AppRoleAssignmentRequired <Boolean>] [-DisplayName <String>] [-ErrorUrl <String>] [-Homepage <String>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]>]
 [-LogoutUrl <String>]
 [-PasswordCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PasswordCredential]>]
 [-PublisherName <String>] [-ReplyUrls <System.Collections.Generic.List`1[System.String]>]
 [-SamlMetadataUrl <String>] [-ServicePrincipalNames <System.Collections.Generic.List`1[System.String]>]
 [-ServicePrincipalType <String>] [-Tags <System.Collections.Generic.List`1[System.String]>]
 [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Create a service principal
```
PS C:\>New-AzureADServicePrincipal -AccountEnabled $true -AppId $MyApp.AppId -AppRoleAssignmentRequired $true -DisplayName $App -Tags {WindowsAzureActiveDirectoryIntegratedApp}
```

This command creates a service principal. The tag "-Tags {WindowsAzureActiveDirectoryIntegratedApp}" is used to have this service principal show up in the list of Integrated Applicatins in the Admin Portal.

## PARAMETERS

### -AccountEnabled
true if the service principal account is enabled; otherwise, false.

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

### -AlternativeNames
The atlernative names for this service principal

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

### -AppId
The unique identifier for the associated application (its appId property).
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppRoleAssignmentRequired
Indicates whether an application role assignment is required.

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

### -ErrorUrl
Specifies the error URL.

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

### -Homepage
Specifies the home page.

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

### -KeyCredentials
The collection of key credentials associated with the service principal.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogoutUrl
Specifies the logout URL.
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

### -PasswordCredentials
Specifies password credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PasswordCredential]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublisherName
Specifies the publisher name.

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

### -ReplyUrls
The URLs that user tokens are sent to for sign in with the associated application, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to for the associated application.

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

### -SamlMetadataUrl
The URL for the SAML metadata

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

### -ServicePrincipalNames
Specifies an array of service principal names. Based on the identifierURIs collection, plus the application's appId property, these URIs are used to reference an application's service principal. A client will use these to:

 ¢â‚¬Â¢ populate requiredResourceAccess, via "Permissions to other applications ¢â‚¬Â in the Azure classic portal.
 ¢â‚¬Â¢ specify a resource URI to acquire an access token, which is the URI returned in the  ¢â‚¬Å"aud ¢â‚¬Â claim.


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

### -ServicePrincipalType
THe type of the service principal

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
Tags linked to this service principal.

Note that if you intend for this service principal to show up in the All Applications list in the admin portal, you need to set this value to {WindowsAzureActiveDirectoryIntegratedApp} 

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)

[Remove-AzureADServicePrincipal](./Remove-AzureADServicePrincipal.md)

[Set-AzureADServicePrincipal](./Set-AzureADServicePrincipal.md)
