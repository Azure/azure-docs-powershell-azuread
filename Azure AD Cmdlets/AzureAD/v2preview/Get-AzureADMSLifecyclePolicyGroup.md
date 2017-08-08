---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADMSLifecyclePolicyGroup

## SYNOPSIS
Retrieves the lifecycle policy object to which a group belongs.

## SYNTAX

```
Get-AzureADMSLifecyclePolicyGroup -Id <String>
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

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

