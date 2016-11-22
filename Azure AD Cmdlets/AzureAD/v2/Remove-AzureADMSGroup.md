---
external help file: azuread.help.xml
online version: https://go.microsoft.com/fwLink/?LinkID=519265&clcid=0x409
schema: 2.0.0
---

# Remove-AzureADMSGroup

## SYNOPSIS
This cmdlet removes a group from the directory

## SYNTAX

```
Remove-AzureADMSGroup [-Id <String>]
```

## DESCRIPTION
Use this cmdlet to remove a group from the directory

## EXAMPLES

### Remove a group
```
Remove-AzureADMSGroup -Id ce0a2213-bd57-4e2f-b9fa-408582e2e260
```

This cmdlet removes the group with Id ce0a2213-bd57-4e2f-b9fa-408582e2e260


This cmdlet has no output

## PARAMETERS

### -Id
The Id of the group that is removed from the directory

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES
Please note that this cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview we may still need to make changes to the cmdlet which could potentially cause unexpected effects.
We discourage customers from using this cmdlet in a production environment.

## RELATED LINKS

