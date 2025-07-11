---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSApplicationVerifiedPublisher

## SYNOPSIS
Removes the verified publisher from an application.

## SYNTAX

```
Remove-AzureADMSApplicationVerifiedPublisher -AppObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
Removes the verified publisher from an application.

## EXAMPLES

### Example 1: Remove the verified publisher from an application.
```
$appObjId = 'ad6c71a5-e48f-4320-bb59-92642a2d8d9f'
          Remove-AzureADMSApplicationVerifiedPublisher -AppObjectId $appObjId
```

## PARAMETERS

### -AppObjectId
The unique identifier of an Azure Active Directory Application object.

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

### string
## OUTPUTS

## NOTES

## RELATED LINKS

[Set-AzureADMSApplicationVerifiedPublisher](Set-AzureADMSApplicationVerifiedPublisher.md)

