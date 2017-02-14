---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserThumbnailPhoto

## SYNOPSIS
Retrieve the thumbnail photo of a user

## SYNTAX

```
Get-AzureADUserThumbnailPhoto -ObjectId <String> [-FilePath <String>] [-FileName <String>] [-View <Boolean>]
 [<CommonParameters>]
```

## DESCRIPTION
Retrieve the thumbnail photo of a user

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADUserThumbnailPhoto -ObjectId df19e8e6-2ad7-453e-87f5-037f6529ae16


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
PropertyIdList       : {11, 274, 305, 306...}
PropertyItems        : {11, 274, 305, 306...}
```

This example shows how to retrieve the thumbnail photo of a user that is specified through the value of the ObejctId parameter

## PARAMETERS

### -FileName
If specified, a copy of the thumbnail photo is written to the specified file name

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
If specified, a copy of the thumbnail photo is written to the specified file path with a random name

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
The object ID of the user for which the thumbnail photo is retrieved

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
If true, view the photo on the screen in a new window

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.Boolean

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

