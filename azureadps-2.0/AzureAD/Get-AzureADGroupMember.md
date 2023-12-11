---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADGroupMember

## SYNOPSIS
Gets a member of a group.

## SYNTAX

```
Get-AzureADGroupMember -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADGroupMember cmdlet gets a member of a group in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a group member by ID
```
PS C:\>Get-AzureADGroupMember -ObjectId "62438306-7c37-4638-a72d-0ee8d9217680"

ObjectId                             ObjectType
--------                             ----------
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 User
```

### Example 2: Get all members within a group by group ID
```
PS C:\> Get-AzureADGroupMember -ObjectId "12431118-5c12-6653-h82e-1ee8d9217682" -All $true

ObjectId                             ObjectType
--------                             ----------
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 User
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 User
0a1068c0-dbb6-4537-9db3-b48f3e31dd76 Group

```


## PARAMETERS

### -All
If true:
	Return all group members.
	
If false: 
	Return the number of objects specified by the Top parameter. 
	If the top parameter is not specified, return the first 100 group members.

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
Specifies the ID of a group in Azure AD.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## NOTES

See the [migration guide for Get-AzureADGroupMember](./migrate/Get-AzureADGroupMember.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS

[Add-AzureADGroupMember](Add-AzureADGroupMember.md)

[Remove-AzureADGroupMember](Remove-AzureADGroupMember.md)

