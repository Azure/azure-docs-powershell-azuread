---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSServicePrincipal

## SYNOPSIS
Updates a service principal.

## SYNTAX

```
Set-AzureADMSServicePrincipal -Id <String> [-AccountEnabled <String>] [-AppId <String>]
 [-AppRoleAssignmentRequired <Boolean>] [-CustomSecurityAttributes <Object>] [-DisplayName <String>]
 [-ErrorUrl <String>] [-LogoutUrl <String>] [-Homepage <String>] [-SamlMetadataUrl <String>]
 [-MicrosoftFirstParty <Boolean>] [-PublisherName <String>] [-PreferredTokenSigningKeyThumbprint <String>]
 [-ReplyUrls <System.Collections.Generic.List`1[System.String]>]
 [-ServicePrincipalNames <System.Collections.Generic.List`1[System.String]>]
 [-Tags <System.Collections.Generic.List`1[System.String]>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsKeyCredential]>]
 [-PasswordCredentials <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsPasswordCredential]>]
 [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSServicePrincipal cmdlet updates a service principal in Azure Active Directory (Azure AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> Set-AzureADMSServicePrincipal -Id 2e0d8ca7-57d1-4a87-9c2a-b3638a4cadbf -AccountEnabled $False
```

This command disables the account of the specified service principal.

### Example 2
```powershell
PS C:\> $attributes = @{
    testAttributeSet1 = @{
        "@odata.type" = "#Microsoft.DirectoryServices.CustomSecurityAttributeValue"
        "testAttribute@odata.type" = "#Collection(String)"
        testAttribute = @("Value3","Value1")
    }
}
PS C:\> Set-AzureADMSServicePrincipal -Id 7d194b0c-bf17-40ff-9f7f-4b671de8dc20 -CustomSecurityAttributes $attributes
```

Assign a custom security attribute with a multi-string value to an application (service principal).
For this example, the attribute set name is `testAttributeSet1` and the custom security attribute name is `testAttribute`.

### Example 3
```powershell
PS C:\> $attributesUpdate = @{
    testAttributeSet1 = @{
        "@odata.type" = "#Microsoft.DirectoryServices.CustomSecurityAttributeValue"
        "testAttribute@odata.type" = "#Collection(String)"
        testAttribute = @("Value5")
    }
}
PS C:\> Set-AzureADMSServicePrincipal -Id 7d194b0c-bf17-40ff-9f7f-4b671de8dc20 -CustomSecurityAttributes $attributesUpdate 
```

Update a custom security attribute with a multi-string value for an application (service principal).
For this example, the attribute set name is `testAttributeSet1` and the custom security attribute name is `testAttribute`.

## PARAMETERS

### -AccountEnabled
Indicates whether the account is enabled.

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

### -AppId
Specifies the application ID.

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

### -CustomSecurityAttributes
Custom security attributes for a service principal.

```yaml
Type: Object
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

### -Id
Specifies the ID of a service principal in Azure AD.

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

### -KeyCredentials
Specifies key credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsKeyCredential]
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

### -MicrosoftFirstParty
Indicates whether the service principal is for a Microsoft first-party app.

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
Specifies password credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.MsPasswordCredential]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferredTokenSigningKeyThumbprint
Preferred token signing key thumbprint for the service principal.

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

### -ServicePrincipalNames
Specifies service principal names.

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

### -Tags
Specifies an array of tags.
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
