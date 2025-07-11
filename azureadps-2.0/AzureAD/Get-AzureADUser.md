---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
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
The Get-AzureADUser cmdlet gets a user from the Microsoft Entra ID.

## EXAMPLES

### Example 1: Get top ten users
```
PS C:\>Get-AzureADUser -Top 10
```

This command gets 10 users.

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

This cmdlet gets all users that match the value of SearchString against the first characters in DisplayName or UserPrincipalName.

### Example 4: Get a user by userPrincipalName
```
PS C:\>Get-AzureADUser -Filter "userPrincipalName eq 'jondoe@contoso.com'"
```

This command gets the specified user.

### Example 5: Get a user by JobTitle
```
PS C:\>Get-AzureADUser -Filter "startswith(JobTitle,'Sales')"
```

This command gets all the users whose job title starts with sales, e.g Sales Manager, and Sales Assistant.

## PARAMETERS

### -All
If true, return all users.
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

### -Filter
Specifies an OData v3.0 filter statement.
This parameter controls which objects are returned.
Details on querying with OData can be found here.
http://www.odata.org/documentation/odata-version-3-0/odata-version-3-0-core-protocol/#queryingcollections. Not all of the OData v3.0 functions and operators are supported at this time.

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
Specifies the ID (as a UPN or ObjectId) of a user in Microsoft Entra ID.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

See the [migration guide for Get-AzureADUser](./migrate/Get-AzureADUser.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[New-AzureADUser](New-AzureADUser.md)

[Remove-AzureADUser](Remove-AzureADUser.md)

[Set-AzureADUser](Set-AzureADUser.md)

