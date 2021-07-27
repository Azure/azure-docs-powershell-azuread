---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADPrivilegedRoleAssignment

## SYNOPSIS
Creates a privileged role assignment for a particular user.

## SYNTAX

```
New-AzureADPrivilegedRoleAssignment [-ExpirationDateTime <DateTime>] [-Id <String>] [-IsElevated <Boolean>]
 [-ResultMessage <String>] -RoleId <String> -UserId <String> [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADPrivilegedRoleAssignment cmdlet creates a privileged role assignment for a particular user.

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ExpirationDateTime
The UTC DateTime when the temporary privileged role assignment will be expired. For permanent role assignment, the value is null.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
The unique identifier for the privileged role assignment.

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

### -IsElevated
`true` if the role assignment is activated. `false` if the role assignment is deactivated.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultMessage
Result message set by the service.

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

### -RoleId
Role identifier, in GUID string format.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserId
User identifier, in GUID string format.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
