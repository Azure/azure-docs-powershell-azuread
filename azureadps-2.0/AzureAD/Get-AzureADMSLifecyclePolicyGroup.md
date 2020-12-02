---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSLifecyclePolicyGroup

## SYNOPSIS
Retrieves the lifecycle policy object to which a group belongs.

## SYNTAX

```
Get-AzureADMSLifecyclePolicyGroup -Id <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSLifecyclePolicyGroup retrieves the lifecycle policy object to which a group belongs.

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSLifecyclePolicyGroup -Id cffd97bd-6b91-4c4e-b553-6918a320211c
```

This command retrieves the lifecycle policy object to which a group belongs.

## PARAMETERS

### -Id
Specifies the ID of a group in Azure Active Directory

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

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
