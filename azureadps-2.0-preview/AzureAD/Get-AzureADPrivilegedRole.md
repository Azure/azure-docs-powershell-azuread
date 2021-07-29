---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADPrivilegedRole

## SYNOPSIS
Read properties and relationships of PrivilegedRole object.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADPrivilegedRole [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADPrivilegedRole -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADPrivilegedRole cmdlet reads the properties and relationships on the privilegedRole object.

## EXAMPLES

## PARAMETERS

### -Filter
Specifies the oData v3.0 filter statement. This parameter controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
The unique identifier for administrator role. It is a GUID string and has the same value as the role template id from Azure AD for the given role.

```yaml
Type: String
Parameter Sets: GetById
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

### System.String

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
