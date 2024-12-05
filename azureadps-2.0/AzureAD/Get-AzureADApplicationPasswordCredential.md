---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADApplicationPasswordCredential

## SYNOPSIS
Gets the password credential for an application.

## SYNTAX

```
Get-AzureADApplicationPasswordCredential -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADApplicationPasswordCredential cmdlet gets the password credentials for an Azure Active Directory application.

## EXAMPLES

### Example 1:
```
PS C:\>Get-AzureADApplicationPasswordCredential -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb

CustomKeyIdentifier :
EndDate             : 9/28/2017 3:57:10 PM
KeyId               :
StartDate           : 9/28/2016 3:57:10 PM
Value               : 
```

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
The objectID of the application for which to get the password credential

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

## NOTES

See the [migration guide for Get-AzureADApplicationPasswordCredential](./migrate/Get-AzureADApplicationPasswordCredential.md) to the Microsoft Graph PowerShell.

## INPUTS

## OUTPUTS

## RELATED LINKS
