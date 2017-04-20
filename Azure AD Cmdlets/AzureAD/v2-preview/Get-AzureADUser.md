---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 52681E27-7FE6-43CE-B2BF-8516C21E04CB
online version: 
schema: 2.0.0
---

# Get-AzureADUser

## SYNOPSIS
Gets a user.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADUser [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADUser [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADUser -ObjectId <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADUser** cmdlet gets a user from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get ten users
```
PS C:\>Get-AzureADUser -Top 10
```

This command gets ten users.

### Example 2: Get a user by ID
```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```

This command gets the specified user.

### Example 3: Search among retrieved users
```
PS C:\> Get-AzureADUser -SearchString "New"

ObjectId                             DisplayName UserPrincipalName                   UserType
--------                             ----------- -----------------                   --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    NewUser@contoso.onmicrosoft.com     Member
2b450b8e-1db6-42cb-a545-1b05eb8a358b New user    NewTestUser@contoso.onmicrosoft.com Member
```

This cmdlet gets all users that match the value of *SearchString* against the first characters in **DisplayName** or **UserPrincipalName** .

## PARAMETERS

### -All
If true, return all users. If false, return the number of objects specified by the Top parameter

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

### -Filter
Specifies an oData v3.0 filter statement. This parameter controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
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
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.
```yaml
Type: String
Parameter Sets: GetVague
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
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

[New-AzureADUser](./New-AzureADUser.md)

[Remove-AzureADUser](./Remove-AzureADUser.md)

[Set-AzureADUser](./Set-AzureADUser.md)
