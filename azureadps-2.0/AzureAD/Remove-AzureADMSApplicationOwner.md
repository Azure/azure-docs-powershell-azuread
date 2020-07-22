---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSApplicationOwner

## SYNOPSIS
Removes an owner from an application object.

## SYNTAX

```
Remove-AzureADMSApplicationOwner -ObjectId <String> -OwnerId <String> [<CommonParameters>]
```

## DESCRIPTION
Removes an owner from an application object.

## EXAMPLES

### Example 1: Remove an owner from an application
```
PS C:\>Remove-AzureADMSApplicationOwner -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84" -OwnerId "c13dd34a-492b-4561-b171-40fcce2916c5"
```

This command removes the owner from the specified application.

## PARAMETERS

### -ObjectId
Specifies the ID of an application in Azure AD.

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

### -OwnerId
Specifies the ID of the owner.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADMSApplicationOwner]()

[Get-AzureADMSApplicationOwner]()

