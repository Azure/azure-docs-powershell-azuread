---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: C62F46A7-EEE7-41C9-9F71-98C05C11E20D
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Get-AzureADMSAuthorizationPolicy

## SYNOPSIS

## SYNTAX

```
Get-AzureADMSAuthorizationPolicy -Id <String> 
```

## DESCRIPTION
The **Get-AzureADMSAuthorizationPolicy** cmdlet gets [authorizationPolicy](https://docs.microsoft.com/graph/api/resources/authorizationpolicy?view=graph-rest-beta) object from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get authorization policy
```
PS C:\>Get-AzureADMSAuthorizationPolicy -id "authorizationPolicy"
```
AuthorizationPolicy is a singleton object, and always exists for the tenant.

## PARAMETERS

### -Id
The Id of the policy for which you want to find the objects

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

## OUTPUTS

## NOTES

## RELATED LINKS
