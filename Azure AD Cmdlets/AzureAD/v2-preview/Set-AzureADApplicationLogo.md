---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADApplicationLogo

## SYNOPSIS
Sets the logo for an Application

## SYNTAX

### File (Default)
```
Set-AzureADApplicationLogo [-ObjectId <String>] -FilePath <String> [<CommonParameters>]
```

### Stream
```
Set-AzureADApplicationLogo [-ObjectId <String>] -FileStream <Stream> [<CommonParameters>]
```

### ByteArray
```
Set-AzureADApplicationLogo [-ObjectId <String>] -ImageByteArray <Byte[]> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to set the logo for an application

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Set-AzureADApplicationLogo -ObjectId 79592454-dea7-4660-9d91-f1768e5055ac -FilePath D:\applogo.jpg
```

This cmdlet sets the application logo for the application specified by the the ObjectID parameter to the image specified with the FIlepath parameter

## PARAMETERS

### -FilePath
The file path of the file that is to be uploaded as the application logo

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
A fileStream that is to be used as the application logo

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
And ImageByteArray that is to be used as the application logo

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
The ObjectID of the Application for which the logo is set

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

