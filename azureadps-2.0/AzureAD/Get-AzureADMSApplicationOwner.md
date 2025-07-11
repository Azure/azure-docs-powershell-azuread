---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSApplicationOwner

## SYNOPSIS
Retrieves the list of owners for an application object.

## SYNTAX

```
Get-AzureADMSApplicationOwner -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves the list of owners for an application object.

## EXAMPLES

### Example 1: Get the owner of an application
```
PS C:\>Get-AzureADMSApplicationOwner -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -Top 1

          ObjectId                             ObjectType
          --------                             ----------
          c13dd34a-492b-4561-b171-40fcce2916c5 User
```

This command gets the owner of an application.

### Example 1: Get the owners of an application
```
PS C:\>Get-AzureADMSApplicationOwner -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -All $true

          ObjectId                             ObjectType
          --------                             ----------
          c13dd34a-492b-4561-b171-40fcce2916c5 User
```

This command gets the owners of an application.

## PARAMETERS

### -ObjectId
Specifies the ID of an application in the Microsoft Entra ID.

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

### -All
If true, return all owners.
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

## INPUTS

### bool?
### int?
### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.GetDirectoryObjectsResponse

## NOTES

See the [migration guide for Get-AzureADMSApplicationOwner](./migrate/Get-AzureADMSApplicationOwner.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Add-AzureADMSApplicationOwner](Add-AzureADMSApplicationOwner.md)

[Remove-AzureADMSApplicationOwner](Remove-AzureADMSApplicationOwner.md)
