---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 547BE76A-9D1F-4DF2-A3FB-BA6E735CD556
---

# Set-AzureADApplication

## SYNOPSIS
Updates a specific application in Azure Active Directory

## SYNTAX

```
Set-AzureADApplication -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
 [-AppRoles <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AppRole]>]
 [-AvailableToOtherTenants <Boolean>] [-DisplayName <String>] [-ErrorUrl <String>] [-Homepage <String>]
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

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\>Set-AzureADApplication -ObjectId 3ddd22e7-a150-4bb3-b100-e410dea1cb84 -DisplayName "New Name"
```

## PARAMETERS

### -ObjectId
The unique idenfier of an application in Azure Active Directory

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

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

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

### -AppRoles
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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

### -KeyCredentials
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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
@{Text=}

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


