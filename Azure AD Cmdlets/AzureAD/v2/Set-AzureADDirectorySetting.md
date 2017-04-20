---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
ms.assetid: 96F47B05-3D04-4298-9C60-03B60B8AD6AF
online version: 
schema: 2.0.0
---

# Set-AzureADDirectorySetting

## SYNOPSIS
Updates a directory setting in Azure Active Directory.

## SYNTAX

```
Set-AzureADDirectorySetting -Id <String> -DirectorySetting <DirectorySetting>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADDirectorySetting** cmdlet updates a directory setting in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -DirectorySetting
Specifies the directory settings.

```yaml
Type: DirectorySetting
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the ID of a settings object in Azure AD.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDirectorySetting](./Get-AzureADDirectorySetting.md)

[New-AzureADDirectorySetting](./New-AzureADDirectorySetting.md)

[Remove-AzureADDirectorySetting](./Remove-AzureADDirectorySetting.md)
