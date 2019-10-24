---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-AzureADUserThumbnailPhoto

## SYNOPSIS
Set the thumbnail photo for a user

## SYNTAX

### File (Default)
```
Set-AzureADUserThumbnailPhoto [-ObjectId <String>] -FilePath <String> [<CommonParameters>]
```

### Stream
```
Set-AzureADUserThumbnailPhoto [-ObjectId <String>] -FileStream <Stream> [<CommonParameters>]
```

### ByteArray
```
Set-AzureADUserThumbnailPhoto [-ObjectId <String>] -ImageByteArray <Byte[]> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to set the thumbnail photo for a user

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Set-AzureADUserThumbnailPhoto -ObjectId ba6752c4-6a2e-4be5-a23d-67d8d5980796 -FilePath D:\UserThumbnailPhoto.jpg
```

This example sets the thumbnail photo of the user specified with the ObjectId parameter to the image specified with the FilePath parameter

## PARAMETERS

### -FilePath
The file path of the image to be uploaded as the user thumbnail photo

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FileStream
A filestream that contains the user thumbnail photo
```yaml
Type: Stream
Parameter Sets: Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ImageByteArray
An Image Byte Array that contains the user thumbnail photo

```yaml
Type: Byte[]
Parameter Sets: ByteArray
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
The Object ID of the user for which the user thumbnail photo is set

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.IO.Stream
System.Byte[]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

