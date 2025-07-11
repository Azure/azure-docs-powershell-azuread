---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSApplicationExtensionProperty

## SYNOPSIS
Retrieves the list of extension properties on an application object.

## SYNTAX

```
Get-AzureADMSApplicationExtensionProperty -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
Retrieves the list of extension properties on an application object.

## EXAMPLES

### Example 1: Get extension properties
```
PS C:\>Get-AzureADMSApplicationExtensionProperty -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"

          ObjectId                             Name                                                    TargetObjects
          --------                             ----                                                    -------------
          344ed560-f8e7-410e-ab9f-c795a7df5c36 extension_36ee4c6c081240a2b820b22ebd02bce3_NewAttribute {}
```

This command gets the extension properties for the specified application in Azure Active Directory.

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

### Microsoft.Open.MSGraph.Model.GetExtensionPropertiesResponse
## NOTES

## RELATED LINKS

[New-AzureADMSApplicationExtensionProperty](New-AzureADMSApplicationExtensionProperty.md)

[Remove-AzureADMSApplicationExtensionProperty](Remove-AzureADMSApplicationExtensionProperty.md)
