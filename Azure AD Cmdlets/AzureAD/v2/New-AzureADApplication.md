---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 235D5FBC-E726-4F95-8BBD-454E8180576A
online version: 
schema: 2.0.0
---

# New-AzureADApplication

## SYNOPSIS
Creates an application.

## SYNTAX

```
New-AzureADApplication [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-AppRoles <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AppRole]>]
 [-AvailableToOtherTenants <Boolean>] -DisplayName <String> [-ErrorUrl <String>] [-Homepage <String>]
 [-IdentifierUris <System.Collections.Generic.List`1[System.String]>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]>]
 [-KnownClientApplications <System.Collections.Generic.List`1[System.String]>] [-LogoutUrl <String>]
 [-MainLogo <Byte[]>] [-Oauth2AllowImplicitFlow <Boolean>] [-Oauth2AllowUrlPathMatching <Boolean>]
 [-Oauth2Permissions <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.OAuth2Permission]>]
 [-OAuth2RequiredPostResponse <Boolean>]
 [-PasswordCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.PasswordCredential]>]
 [-PublicClient <Boolean>] [-ReplyUrls <System.Collections.Generic.List`1[System.String]>]
 [-RequiredResourceAccess <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.RequiredResourceAccess]>]
 [-SamlMetadataUrl <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADApplication** cmdlet creates an application in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Create an application
```
PS C:\>New-AzureADApplication -DisplayName "My new application"  -IdentifierUris "http://mynewapp.contoso.com"

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
acd10942-5747-4385-8824-4c5d5fa904f9 b5fecfab-0ea2-4fd1-8570-b2c41b3d5149 My new application
```

This command creates an application in Azure AD.

## PARAMETERS

### -AppRoles
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AppRole]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableToOtherTenants
Indicates whether this application is available in other tenants.

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
Specifies the display name of the application.

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

### -ErrorUrl
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

### -IdentifierUris
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

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredentials
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

### -KnownClientApplications
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

### -LogoutUrl
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

### -MainLogo
```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oauth2AllowImplicitFlow
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

### -Oauth2AllowUrlPathMatching
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

### -Oauth2Permissions
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.OAuth2Permission]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OAuth2RequiredPostResponse
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

### -PasswordCredentials
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

### -PublicClient
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

### -ReplyUrls
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

### -RequiredResourceAccess
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.RequiredResourceAccess]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SamlMetadataUrl
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADApplication](./Get-AzureADApplication.md)

[Remove-AzureADApplication](./Remove-AzureADApplication.md)

[Set-AzureADApplication](./Set-AzureADApplication.md)


