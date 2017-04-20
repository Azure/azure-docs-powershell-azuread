---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: 98A2D6B6-FBE5-420F-BA31-94161FBACEDF
online version: 
schema: 2.0.0
---

# Get-AzureADUserExtension

## SYNOPSIS
Gets a user extension.

## SYNTAX

```
Get-AzureADUserExtension -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADUserExtension** cmdlet gets a user extension in Azure Active Directory (AD).

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

The first command gets the ID of an Azure AD user by using the [Get-AzureADUser](./Get-AzureADUser.md) cmdlet. 
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUser](./Get-AzureADUser.md)

[Remove-AzureADUserExtension](./Remove-AzureADUserExtension.md)

[Set-AzureADUserExtension](./Set-AzureADUserExtension.md)
