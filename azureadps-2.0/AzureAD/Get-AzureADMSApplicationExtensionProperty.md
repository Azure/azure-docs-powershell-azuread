---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
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
PS C:\>Get-AzureADMSApplicationExtensionProperty -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84"

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

[New-AzureADMSApplicationExtensionProperty]()

[Remove-AzureADMSApplicationExtensionProperty]()

