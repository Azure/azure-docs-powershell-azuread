---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSApplication

## SYNOPSIS
Deletes an application object.

## SYNTAX

```
Remove-AzureADMSApplication -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
Deletes an application object identified by objectId.

## EXAMPLES

### Example 1: Remove an application
```
PS C:\>Remove-AzureADMSApplication -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"
```

This command removes the specified application.

## PARAMETERS

### -ObjectId
The unique identifier of the object specific Azure Active Directory object

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

[Get-AzureADMSApplication](Get-AzureADMSApplication.md)

[New-AzureADMSApplication](New-AzureADMSApplication.md)

[Set-AzureADMSApplication](Set-AzureADMSApplication.md)
