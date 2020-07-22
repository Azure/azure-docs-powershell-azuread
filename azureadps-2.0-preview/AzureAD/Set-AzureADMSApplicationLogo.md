---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSApplicationLogo

## SYNOPSIS
Sets the logo for an application object.

## SYNTAX

```
Set-AzureADMSApplicationLogo -ObjectId <String> -Content <Byte[]> [<CommonParameters>]
```

## DESCRIPTION
Sets the logo for an application object.

## EXAMPLES

### Example 1: Sets the logo of the application
```
PS C:\>Set-AzureADMSApplicationLogo -ObjectId 121ce3aa-64cb-44f2-99e8-deb705caeddd -Content {imagebytearray}
```

This command updates the application logo.

## PARAMETERS

### -ObjectId
The unique identifier of the object specific Azure Active Directory object

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

### -Content
An ImageByteArray that is to be used as the application logo

```yaml
Type: Byte[]
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
### Byte[]
## OUTPUTS

## NOTES

## RELATED LINKS
