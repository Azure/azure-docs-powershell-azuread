---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADApplicationProxyConnectorGroup

## SYNOPSIS
The Set-AzureADApplicationProxyConnectorGroup cmdlet allows you to change the name of a given Application Proxy connector group.

## SYNTAX

```
Set-AzureADApplicationProxyConnectorGroup -Id <String> -Name <Name> [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADApplicationProxyConnectorGroup cmdlet allows you to change the name of a given Application Proxy connector group.

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADApplicationProxyConnectorGroup -Id d533d7b1-fd92-49e8-a200-3e7dcf7c2ab5 -Name "Offsite Application Servers"
```

Example 1: Rename a Connector Group to "Offsite Application Servers"

## PARAMETERS

### -Id
The unique identifier of the Connector group that will be renamed.
You can find the Id using the Get-AzureADApplicationProxyConnectorGroup command.

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

### -Name
The new name for the Connector group.

```yaml
Type: Name
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

### System.String
Microsoft.Open.MSGraph.Model.Name

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
