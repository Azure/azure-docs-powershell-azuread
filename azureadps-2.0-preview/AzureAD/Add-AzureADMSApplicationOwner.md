---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMSApplicationOwner

## SYNOPSIS
Adds an owner for an application object.

## SYNTAX

```
Add-AzureADMSApplicationOwner -ObjectId <String> -RefObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
Adds an owner for an application object.

## EXAMPLES

### Example 1: Add an owner to an application
```
PS C:\>Add-AzureADMSApplicationOwner -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -RefObjectId bbbbbbbb-1111-2222-3333-cccccccccccc
```

This command adds an owner to an application.

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

### -RefObjectId
The unique identifier of the specific Azure Active Directory object that will be assigned as owner/manager/member

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

[Get-AzureADMSApplicationOwner]()

[Remove-AzureADMSApplicationOwner]()
