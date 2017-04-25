---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Revoke-AzureADSignedInUserAllRefreshToken

## SYNOPSIS
Invalidates the refresh tokens issued to applications for the current user. 

## SYNTAX

```
Revoke-AzureADSignedInUserAllRefreshToken [<CommonParameters>]
```

## DESCRIPTION
The **Revoke-AzureADSignedInUserAllRefreshToken** cmdlet invalidates the refresh tokens issued to applications for the current user. 
The cmdlet also invalidates tokens issued to session cookies in a browser for the user. 
The cmdlet operates by resetting the **refreshTokensValidFromDateTime** user property to the current date and time.

## EXAMPLES

### Example 1: Revoke refresh tokens for the current user
```
PS C:\> Revoke-AzureADSignedInUserAllRefreshToken
```

This command revokes the tokens for the current user. 

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Revoke-AzureADUserAllRefreshToken](./Revoke-AzureADUserAllRefreshToken.md)

[#AzureAD: Certificate based authentication for iOS and Android now in preview!](https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/)
