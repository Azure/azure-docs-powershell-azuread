---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserOAuth2PermissionGrant

## SYNOPSIS
Gets an oAuth2PermissionGrant object.

## SYNTAX

```
Get-AzureADUserOAuth2PermissionGrant -ObjectId <String> [-All <Boolean>] [-Top <Int32>]
```

## DESCRIPTION
The Get-AzureADUserOAuth2PermissionGrant cmdlet gets an oAuth2PermissionGrant object for the specified user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve the OAuth2 permission grants for a user
```
PS C:\> $UserId = (Get-AzureADUser -Top 1).ObjectId
PS C:\> Get-AzureADUserOAuth2PermissionGrant -ObjectId $UserId
```

The first command gets the ID of an Azure AD user by using the Get-AzureADUser (./Get-AzureADUser.md)cmdlet. 
The command stores the value in the $UserId variable.

The second command gets the OAuth2 permission grants for the user identified by $UserId.

## PARAMETERS

### -All
If true, return all permission grants.
If false, return the number of objects specified by the Top parameter

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
Specifies the ID (as a UPN or ObjectId) of a user in Azure AD.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUser]()

