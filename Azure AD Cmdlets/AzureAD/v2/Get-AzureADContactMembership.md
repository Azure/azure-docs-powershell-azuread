---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: DB181096-FF93-4C1E-9E08-884E8162DAB7
online version: 
schema: 2.0.0
---

# Get-AzureADContactMembership

## SYNOPSIS
Get a contact membership.

## SYNTAX

```
Get-AzureADContactMembership -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADContactMembership** cmdlet gets a contact membership in Azure Active Directory.

## EXAMPLES

### Example 1: Get the memberships of a contact
```
PS C:\> $Contact = Get-AzureADContact -Top 1
PS C:\> Get-AzureADContactMembership -ObjectId $Contact.ObjectId

ObjectId                             ObjectType
--------                             ----------
0015df25-808e-4715-9c24-a6929c25c201 Group
```

The first command gets a contact by using the [Get-AzureADContact](./Get-AzureADContact.md) cmdlet, and then stores it in the $Contact variable.

The second command gets the memberships for $Contact.

## PARAMETERS

### -All
If true, return all memberships. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of a contact in Azure Active Directory.

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

[Get-AzureADContact](./Get-AzureADContact.md)
