---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 18D86E76-31D1-4286-8950-8067FBAF005A
online version: 
schema: 2.0.0
---

# Get-AzureADUserMembership

## SYNOPSIS
Get user memberships.

## SYNTAX

```
Get-AzureADUserMembership -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADUserMembership** cmdlet gets user memberships in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get user memberships
```
PS C:\>Get-AzureADUserMembership  -ObjectId "df19e8e6-2ad7-453e-87f5-037f6529ae16"

ObjectId                             ObjectType
--------                             ----------
019ea7a2-1613-47c9-81cb-20ba35b1ae48 Role
ef58cdc0-3e08-4e02-ab16-db99ef8dfa49 Group
52b94dfa-293a-496c-b98e-e16a20247065 Group
a7cf942b-248c-4bec-9f52-f1a6493959c4 Group
31dba078-ade5-4f97-ac38-3b2edb1af6e0 Group
8c6a5c45-e93e-4f2b-81be-b57ad4c43ddd Role
d96eb2b3-0970-4827-8f26-6008efd86511 Role
9c2564d6-e4d7-4167-a79f-4b961512f232 Group
36db8aaf-022a-448d-aedc-34ef2ceb943c Group
0e6cf869-82ca-4647-b330-420b9a6f8ef7 Group
78045c26-218e-46fb-94b6-1a47320da153 Group
093fc0e2-1d6e-4a1b-9bf8-effa0196f1f7 Group
```

This command gets the memberships for the specified user.

## PARAMETERS

### -All
If true, return all memberships of this user. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a user (as a UPN or ObjectId) in Azure AD. 

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

