---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: 45C6B663-1AD4-4ED3-81BB-D2B79C67BC47
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Get-AzureADApplicationOwner

## SYNOPSIS
Gets the owner of an application.

## SYNTAX

```
Get-AzureADApplicationOwner -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADApplicationOwner** cmdlet get an owner of an Azure Active Directory application.

## EXAMPLES

### Example 1: Get the owner of an application
```
PS C:\>Get-AzureADApplicationOwner -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84"

ObjectId                             ObjectType
--------                             ----------
c13dd34a-492b-4561-b171-40fcce2916c5 User
```

This command gets the owner of an application.

## PARAMETERS

### -All
If true, return all owners. If false, return the number of objects specified by the Top parameter

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
Specifies the ID of an application in Azure Active Directory.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADApplicationOwner](./Add-AzureADApplicationOwner.md)
[Remove-AzureADApplicationOwner](./Remove-AzureADApplicationOwner.md)

