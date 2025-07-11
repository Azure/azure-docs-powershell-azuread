---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSApplicationExtensionProperty

## SYNOPSIS
Creates an extension property on an application object.

## SYNTAX

```
New-AzureADMSApplicationExtensionProperty -ObjectId <String> [-Name <String>] [-DataType <String>]
 [-TargetObjects <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
Creates an extension property on an application object.

## EXAMPLES

### Example 1: Create an extension property
```
PS C:\>New-AzureADMSApplicationExtensionProperty -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb" -DataType "string" -Name "NewAttribute" -TargetObjects "Application"


          ObjectId                             Name                                                    TargetObjects
          --------                             ----                                                    -------------
          aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb extension_36ee4c6c081240a2b820b22ebd02bce3_NewAttribute {}
```

This command creates an application extension property of the string type for the specified object.

## PARAMETERS

### -DataType
Specifies the data type of the extension property.

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

### -Name
Specifies the data type of the extension property.

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

### -TargetObjects
Specifies target objects.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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

### string
### System.Collections.Generic.List`1[System.String]
## OUTPUTS

### Microsoft.Open.MSGraph.Model.ExtensionProperty
## NOTES

## RELATED LINKS

[Get-AzureADMSApplicationExtensionProperty](Get-AzureADMSApplicationExtensionProperty.md)

[Remove-AzureADMSApplicationExtensionProperty](Remove-AzureADMSApplicationExtensionProperty.md)
