---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
Module Name:
online version:
schema: 2.0.0
---

# Set-AzureADMSTrustFrameworkPolicy

## SYNOPSIS
This cmdlet is used to update a trust framework policy (custom policy) in the directory.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-AzureADMSTrustFrameworkPolicy -Content <String> [-Id <String>] [-OutputFilePath <String>]
 [<CommonParameters>]
```

### UNNAMED_PARAMETER_SET_2
```
Set-AzureADMSTrustFrameworkPolicy [-Id <String>] -InputFilePath <String> [-OutputFilePath <String>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to update a trust framework policy in the directory.

The contents of the trust framework policy to be updated can be provided using a file or a command line variable.

The contents of the updated trust framework policy can be written to an output file or to the screen.

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin -Content $policyContent
```

The example updates a trust framework policy from the content specified.

The contents of updated trust framework policy are displayed on screen.

### Example 2
```
PS C:\> Set-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin -Content $policyContent -OutputFilePath C:\CreatedPolicy.xml
```

The example updates a trust framework policy from the content specified.

The contents of updated trust framework policy are written to file mentioned in output file path.

### Example 3
```
PS C:\> Set-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin -InputFilePath C:\InputPolicy.xml -OutputFilePath C:\CreatedPolicy.xml
```

The example updates a trust framework policy from the file mentioned in InputFilePath.

The contents of updated trust framework policy are written to file mentioned in output file path.

### Example 4
```
PS C:\> Set-AzureADMSTrustFrameworkPolicy -Id B2C_1A_signup_signin -InputFilePath C:\InputPolicy.xml
```

The example updates a trust framework policy from the file mentioned in InputFilePath.

The contents of updated created trust framework policy are displayed on screen.

## PARAMETERS

### -Content
The content of the trust framework policy to be updated.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
The unique identifier for a trust framework policy.

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

### -InputFilePath
Path to the file used for reading the contents of trust framework policy to be updated.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -OutputFilePath
Path to the file used for writing the contents of updated trust framework policy.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
