---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADMSApplicationExtensionProperty

## SYNOPSIS
Deletes an extension property from an application object.

## SYNTAX

```
Remove-AzureADMSApplicationExtensionProperty -ObjectId <String> -ExtensionPropertyId <String>
 [<CommonParameters>]
```

## DESCRIPTION
Deletes an extension property from an application object.

## EXAMPLES

### Example 1: Remove an extension property
```
PS C:\> Remove-AzureADMSApplicationExtensionProperty -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -ExtensionPropertyId "344ed560-f8e7-410e-ab9f-c79df5c36"
```

This command removes the extension property that has the specified ID from an application in Azure Active Directory.

## PARAMETERS

### -ObjectId
Specifies the unique ID of an application in Azure Active Directory.

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

### -ExtensionPropertyId
Specifies the unique ID of the extension property to remove.

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

[Get-AzureADMSApplicationExtensionProperty](Get-AzureADMSApplicationExtensionProperty.md)

[New-AzureADMSApplicationExtensionProperty](New-AzureADMSApplicationExtensionProperty.md)
