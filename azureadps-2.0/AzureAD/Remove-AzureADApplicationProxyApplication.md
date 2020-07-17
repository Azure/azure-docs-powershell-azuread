---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationProxyApplication

## SYNOPSIS
Deletes an Application Proxy application.

## SYNTAX

```
Remove-AzureADApplicationProxyApplication -ObjectId <String> [-RemoveADApplication <Boolean>]
```

## DESCRIPTION
The Remove-AzureADApplicationProxyApplication cmdlet removes Application Proxy configurations from a specific application in Azure Active Directory, and can delete the application completely if specified.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADApplicationProxyApplication -ObjectId 257098d1-f8dd-4efb-88a2-1c92d3654f10
```

Example 1: Remove a Proxy Application

### Example 2
```
PS C:\> Remove-AzureADApplicationProxyApplication -ObjectId 0d7b0f02-3f63-414d-8d20-4b8bd0291e42 -RemoveADApplication $true
```

Example 2: Remove a Proxy Application, and remove it from Azure AD completely

## PARAMETERS

### -ObjectId
The unique application Id of the application. This can be found using the Get-AzureADApplication command. You can also find this in the Azure Portal by navigating to AAD, Enterprise Applications, All Applications, Select your application, go to the properties tab, and use the ObjectId on that page. 

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

### -RemoveADApplication
This allows you to delete application completely. When this is false (default), Application Proxy properties are removed from the application but the application still exists. If this is true, the application is completely removed from Azure AD.

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

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

