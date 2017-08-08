---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Reset-AzureADMSLifeCycleGroup

## SYNOPSIS
Renews a group by updating the RenewedDateTime property on a group to the current DateTime.

## SYNTAX

```
Reset-AzureADMSLifeCycleGroup -GroupId <String>
```

## DESCRIPTION
The Reset-AzureADMSLifeCycleGroup renews a group by updating the RenewedDateTime property on a group to the current DateTime. When a group is renewed, the group expiration is extended by the number of days defined in the policy.

## EXAMPLES

### Example 1
```
PS C:\> Reset-AzureADMSLifeCycleGroup -groupId cffd97bd-6b91-4c4e-b553-6918a320211c
```

The Reset-AzureADMSLifeCycleGroup renews a specified group by updating the RenewedDateTime property on a group to the current DateTime.

## PARAMETERS

### -GroupId
Specifies the ID of a group in Azure Active Directory.

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

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

