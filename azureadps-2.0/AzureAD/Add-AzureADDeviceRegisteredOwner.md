---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Add-AzureADDeviceRegisteredOwner

## SYNOPSIS
Adds a registered owner for a device.

## SYNTAX

```
Add-AzureADDeviceRegisteredOwner -ObjectId <String> -RefObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADDeviceRegisteredOwner cmdlet adds a registered owner for an Azure Active Directory device.

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ObjectId
Specifies the object ID.

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

### -RefObjectId
Specifies the ID of the Active Directory object to add.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDeviceRegisteredOwner]()

[Remove-AzureADDeviceRegisteredOwner]()

