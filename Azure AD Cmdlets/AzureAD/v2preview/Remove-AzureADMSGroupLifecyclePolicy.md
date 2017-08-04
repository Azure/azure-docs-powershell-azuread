---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureADMSGroupLifecyclePolicy

## SYNOPSIS
Deletes a groupLifecyclePolicies object

## SYNTAX

```
Remove-AzureADMSGroupLifecyclePolicy -Id <String>
```

## DESCRIPTION
The Remove-AzureADMSGroupLifecyclePolicy command deletes a groupLifecyclePolicies object in Azure Active Directory.

## EXAMPLES

### Example 1
```
PS C:\> Remove-AzureADMSGroupLifecyclePolicy -Id "13bed58e-6144-41e5-abbd-47c95964e671"
```

This cmdlet deletes the groupLifecyclePolicies object that has the specified ID.

## PARAMETERS

### -Id
Specifies the ID of the groupLifecyclePolicies object that this cmdlet removes.

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

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

