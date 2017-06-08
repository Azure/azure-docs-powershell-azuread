---
external help file: Microsoft.Open.Azure.AD.CommonLibrary.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADCurrentSessionInfo

## SYNOPSIS
This cmdlet will return the current session state

## SYNTAX

```
Get-AzureADCurrentSessionInfo [-WhatIf] [-Confirm]
```

## DESCRIPTION
This cmdlet will return the current session state

## EXAMPLES

### Example 1
```
Get-AzureADCurrentSessionInfo

Account                       Environment TenantId
-------                       ----------- --------
Karen@drumkit.onmicrosoft.com AzureCloud  85b5ff1e-0402-400c-9e3c-0f9e965325d1
```

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

