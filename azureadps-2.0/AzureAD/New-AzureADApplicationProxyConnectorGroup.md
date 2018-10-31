---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureADApplicationProxyConnectorGroup

## SYNOPSIS
The New-AzureADApplicationProxyConnectorGroup cmdlet creates a new Application Proxy Connector group. 

## SYNTAX

```
New-AzureADApplicationProxyConnectorGroup -Name <Name>
```

## DESCRIPTION
The New-AzureADApplicationProxyConnectorGroup cmdlet creates a new Application Proxy connector group. 

## EXAMPLES

### Example 1
```
PS C:\> New-AzureADApplicationProxyConnectorGroup -Name "Backup Application Servers"

Id                                   Name                       ConnectorGroupType IsDefault
--                                   ----                       ------------------ ---------
d533d7b1-fd92-49e8-a200-3e7dcf7c2ab5 Backup Application Servers applicationProxy       False 
```
Example 1: Create a new Connector Group with the name "Backup Application Servers"

## PARAMETERS

### -Name
The name of the new Connector Group.

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

## INPUTS

### Microsoft.Open.MSGraph.Model.Name


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

