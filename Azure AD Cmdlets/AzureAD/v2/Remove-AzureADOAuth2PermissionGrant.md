---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADOAuth2PermissionGrant

## SYNOPSIS
Delete an oAuth2PermissionGrant.

## SYNTAX

```
Remove-AzureADOAuth2PermissionGrant -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove an OAuth2 permission grant.
```
$SharePointSP = Get-AzureADServicePrincipal | Where-Object {$_.DisplayName -eq "Microsoft.SharePoint"}
$SharePointOA2AllSitesRead = Get-AzureADOAuth2PermissionGrant | Where-Object {$_.ResourceId -eq $SharePointSP.ObjectId} | Where-Object {$_.Scope -eq "AllSites.Read"}
Remove-AzureADOAuth2PermissionGrant -ObjectId $SharePointOA2AllSitesRead.ObjectId
```

## PARAMETERS

### -ObjectId
The unique identifier of an oAuth2PermissionGrant in Azure Active Directory

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

