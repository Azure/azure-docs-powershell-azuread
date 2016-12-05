---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: E02E6FAA-5FE3-4EDC-8BCA-75342557F3D5
online version: 
schema: 2.0.0
---

# Remove-AzureADOAuth2PermissionGrant

## SYNOPSIS
Removes an oAuth2PermissionGrant.

## SYNTAX

```
Remove-AzureADOAuth2PermissionGrant -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADOAuth2PermissionGrant** cmdlet removes an **oAuth2PermissionGrant** object in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove an OAuth2 permission grant
```
PS C:\> $SharePointSP = Get-AzureADServicePrincipal | Where-Object {$_.DisplayName -eq "Microsoft.SharePoint"}
PS C:\> $SharePointOA2AllSitesRead = Get-AzureADOAuth2PermissionGrant | Where-Object {$_.ResourceId -eq $SharePointSP.ObjectId} | Where-Object {$_.Scope -eq "AllSites.Read"}
PS C:\> Remove-AzureADOAuth2PermissionGrant -ObjectId $SharePointOA2AllSitesRead.ObjectId
```

The first command gets a service principal that matches the specified display name by using the [Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md) cmdlet. 
The command stores the result in the $SharePointSP variable.

The second command gets certain permission grants by using the [Get-AzureADOAuth2PermissionGrant](./Get-AzureADOAuth2PermissionGrantmd) cmdlet. 
The command stores the result in the $SharePointOA2AllSitesRead variable.

The final command removes the permission grant in $SharePointOA2AllSitesRead.

## PARAMETERS

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

### -ObjectId
Specifies the ID of an **oAuth2PermissionGrant** object in Azure AD.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADOAuth2PermissionGrant](./Get-AzureADOAuth2PermissionGrant.md)

[Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)
