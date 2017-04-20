---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: DCED77C4-3206-40A8-A5CA-7A08B9EBA1CF
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalOAuth2PermissionGrant

## SYNOPSIS
Gets an oAuth2PermissionGrant object.

## SYNTAX

```
Get-AzureADServicePrincipalOAuth2PermissionGrant -ObjectId <String> [-All <Boolean>] [-Top <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADServicePrincipalOAuth2PermissionGrant** cmdlet gets an **oAuth2PermissionGrant** object for a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve the OAuth2 permission grants of a service principal
```
PS C:\> ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> Get-AzureADServicePrincipalOAuth2PermissionGrant -ObjectId $ServicePrincipalId
```

The first command gets the ID of a service principal by using the [Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md) cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets the OAuth2 permission grants of a service principal identified by $ServicePrincipalId. 

## PARAMETERS

### -All
If true, return all permission grants. If false, return the number of objects specified by the Top parameter

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

### -ObjectId
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

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
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

[Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)
