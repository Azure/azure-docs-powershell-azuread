---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADMSGroupLifecyclePolicy

## SYNOPSIS
Retrieves the properties and relationships of a groupLifecyclePolicies object in Azure Active Directory

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSGroupLifecyclePolicy [-All <Boolean>]
```

### GetById
```
Get-AzureADMSGroupLifecyclePolicy -Id <String> [-All <Boolean>]
```

## DESCRIPTION
The Get-AzureADMSGroupLifecyclePolicy command retrieves the properties and relationships of a groupLifecyclePolicies object in Azure Active Directory

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSGroupLifecyclePolicy
```

This command retrieves the group expiration settings configured for the tenant

## PARAMETERS

### -All
Get all groupLifecyclePolicies objects in Azure Active Directory

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
Specifies the ID of a groupLifecyclePolicies object in Azure Active Directory

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

## INPUTS

### System.String
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

