---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
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
PS C:\>Remove-AzureADMSApplicationOwner -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -OwnerId "bbbbbbbb-1111-2222-3333-cccccccccccc"
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADMSApplicationOwner]()

[Get-AzureADMSApplicationOwner]()
