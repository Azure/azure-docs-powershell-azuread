---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: 306B2B21-9B1C-4388-B3D6-419CDE02C75C
online version: 
schema: 2.0.0
---

# Get-AzureADApplicationKeyCredential

## SYNOPSIS
Gets the key credentials for an application.

## SYNTAX

```
Get-AzureADApplicationKeyCredential -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADApplicationKeyCredential** cmdlet gets the key credentials for an application.

## EXAMPLES

### Example 1: Get key credentials
```
PS C:\> Get-AzureADApplicationKeyCredential -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84"
```

This command gets the key credentials for the specified application.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

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

### -ObjectId
Specifies a unique ID of an application in Azure Active Directory for which to get key credentials

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

[New-AzureADApplicationKeyCredential](./New-AzureADApplicationKeyCredential.md)

[Remove-AzureADApplicationKeyCredential](./Remove-AzureADApplicationKeyCredential.md)
