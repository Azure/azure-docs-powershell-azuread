---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADPrivilegedRoleAssignment

## SYNOPSIS
Retrieve a list of privilegedRoleAssignment objects, which correspond to all role assignments for the organization.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADPrivilegedRoleAssignment [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

### GetById
```
Get-AzureADPrivilegedRoleAssignment -Id <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADPrivilegedRoleAssignment cmdlet retrieves a list of privilegedRoleAssignment objects, which correspond to all role assignments for the organization.

## EXAMPLES

## PARAMETERS

### -All
If true, return all privilegedRoleAssignments. If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
The unique identifier for the privileged role assignment.

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

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
