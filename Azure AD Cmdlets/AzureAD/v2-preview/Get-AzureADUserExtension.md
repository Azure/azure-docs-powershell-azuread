---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserExtension

## SYNOPSIS
Gets a user extension.

## SYNTAX

```
Get-AzureADUserExtension -ObjectId <String>
```

## DESCRIPTION
The Get-AzureADUserExtension cmdlet gets a user extension in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve extension attributes for a user
```
PS C:\> $UserId = (Get-AzureADUser -Top 1).ObjectId
PS C:\> Get-AzureADUserExtension -ObjectId $UserId

Key                            Value 
---                            ----- 
odata.metadata                 https://graph.windows.net/85b5ff1e-0402-400c-9e3c0f9e965325d1$metadata#directoryObjects/Microsoft.Director... 
odata.type                     Microsoft.DirectoryServices.User
deletionTimestamps
signInNames                    [] 
companyName 
creationType 
facsimileTelephoneNumber 
isCompromised 
refreshTokensValidFromDateTime 11/7/2016 10:11:09 PM 
showInAddressList
```

The first command gets the ID of an Azure AD user by using the Get-AzureADUser (./Get-AzureADUser.md)cmdlet. 
The command stores the value in the $UserId variable.

The second command retrieves all extension attributes that have a value assigned to them for the user identified by $UserId.

## PARAMETERS

### -ObjectId
Specifies the ID of an object.

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

[Get-AzureADUser]()

[Remove-AzureADUserExtension]()

[Set-AzureADUserExtension]()

