---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSTrustFrameworkPolicy

## SYNOPSIS
This cmdlet is used to create a trust framework policy (custom policy) in the directory.

## SYNTAX

### Content (Default)
```
New-AzureADMSTrustFrameworkPolicy [-OutputFilePath <String>] -Content <String> [<CommonParameters>]
```

### File
```
New-AzureADMSTrustFrameworkPolicy -InputFilePath <String> [-OutputFilePath <String>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to create a trust framework policy in the directory.

The contents of the trust framework policy to be created can be provided using a file or a command line variable.

The contents of the created trust framework policy can be written to an output file or to the screen.

## EXAMPLES

### Example 1
```
PS C:\> New-AzureADMSTrustFrameworkPolicy -Content $policyContent
```

The example creates a trust framework policy from the content specified.

The contents of newly created trust framework policy are displayed on screen.

### Example 2
```
PS C:\> New-AzureADMSTrustFrameworkPolicy -Content $policyContent -OutputFilePath C:\CreatedPolicy.xml
```

The example creates a trust framework policy from the content specified.

The contents of newly created trust framework policy are written to file mentioned in output file path.

### Example 3
```
PS C:\> New-AzureADMSTrustFrameworkPolicy -InputFilePath C:\InputPolicy.xml -OutputFilePath C:\CreatedPolicy.xml
```

The example creates a trust framework policy from the file mentioned in InputFilePath.

The contents of newly created trust framework policy are written to file mentioned in output file path.

### Example 4
```
PS C:\> New-AzureADMSTrustFrameworkPolicy -InputFilePath C:\InputPolicy.xml
```

The example creates a trust framework policy from the file mentioned in InputFilePath.

The contents of newly created trust framework policy are displayed on screen.

## PARAMETERS

### -Content
The content of the trust framework policy to be created.

```yaml
Type: String
Parameter Sets: Content
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InputFilePath
Path to the file used for reading the contents of trust framework policy to be created.

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

### -OutputFilePath
Path to the file used for writing the contents of newly created trust framework policy.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
