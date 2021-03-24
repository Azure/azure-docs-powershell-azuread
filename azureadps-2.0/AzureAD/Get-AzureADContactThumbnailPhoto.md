---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADContactThumbnailPhoto

## SYNOPSIS
Retrieves the thumbnail photo of a contact

## SYNTAX

```
Get-AzureADContactThumbnailPhoto -ObjectId <String> [-FilePath <String>] [-FileName <String>] [-View <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION
Retrieves the thumbnail photo of a contact

## EXAMPLES

### Example 1
```
Get-AzureADContactThumbnailPhoto -ObjectId b052db07-e7ec-4c0e-b481-a5ba550b9ee7

Tag                  :
PhysicalDimension    : {Width=279, Height=390}
Size                 : {Width=279, Height=390}
Width                : 279
Height               : 390
HorizontalResolution : 96
VerticalResolution   : 96
Flags                : 77840
RawFormat            : [ImageFormat: b96b3cae-0728-11d3-9d7b-0000f81ef32e]
PixelFormat          : Format24bppRgb
Palette              : System.Drawing.Imaging.ColorPalette
FrameDimensionsList  : {7462dc86-6180-4c7e-8e3f-ee7333a7a483}
PropertyIdList       : {274, 305, 306, 36867...}
PropertyItems        : {274, 305, 306, 36867...}
```

This example retrieves the thumbnail photo of the contact object specified with the object ID parameter

## PARAMETERS

### -FileName
When provided, the cmdlet will write a copy of the thumbnail photo to this filename

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FilePath
When provided, the cmdlet will write a copy of the thumbnail photo to this file path using a random filename

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
The object ID of the contact for which the thumbnail photo is retrieved

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

### -View
If this parameter value is set to $True, display the retrieved thumbnail photo in a new window

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.Boolean

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
