---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 2AB8CC27-F872-4E3D-9972-A4E11BDD4B33
online version: 
schema: 2.0.0
---

# Get-AzureADUserCreatedObject

## SYNOPSIS
Get objects created by the user.

## SYNTAX

```
Get-AzureADUserCreatedObject -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADUserCreatedObject** cmdlet gets objects created by a user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a user-created object
```
PS C:\>Get-AzureADUserCreatedObject -ObjectId "df19e8e6-2ad7-453e-87f5-037f6529ae16"

ObjectId                             ObjectType
--------                             ----------
f618e073-cda3-4fc7-b8bd-5ad63f19840f ServicePrincipal
ed70f968-38ec-48d6-ae58-decfe80bfd5f ServicePrincipal
35ab4659-f61c-4a75-98d2-ef1d04ac2095 ServicePrincipal
d0ce9d42-c943-43a1-a0b0-b1ded8d0ce3d ServicePrincipal
```

This command gets an object created by the specified user.

## PARAMETERS

### -All
If true, return all objects created by this user. If false, return the number of objects specified by the Top parameter

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

