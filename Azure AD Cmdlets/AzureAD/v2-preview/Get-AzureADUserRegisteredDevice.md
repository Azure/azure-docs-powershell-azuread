---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 4A7B644A-221C-48D7-8A20-85511A03D4CD
online version: 
schema: 2.0.0
---

# Get-AzureADUserRegisteredDevice

## SYNOPSIS
Get devices registered by a user.

## SYNTAX

```
Get-AzureADUserRegisteredDevice -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADUserRegisteredDevice** cmdlet gets devices registered by a user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get registered devices
```
PS C:\>Get-AzureADUserRegisteredDevice -ObjectId  "df19e8e6-2ad7-453e-87f5-037f6529ae16"
```

This command gets the devices that are registered to the specified user.

## PARAMETERS

### -All
If true, return all devices for this user

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
Specifies The maximum number of records to return.

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

