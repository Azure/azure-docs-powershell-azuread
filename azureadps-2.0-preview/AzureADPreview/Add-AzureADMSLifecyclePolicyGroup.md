---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Add-AzureADMSLifecyclePolicyGroup

## SYNOPSIS
Adds a group to a lifecycle policy

## SYNTAX

```
Add-AzureADMSLifecyclePolicyGroup -Id <String> -GroupId <String> [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADMSLifecyclePolicyGroup cmdlet adds a group to a lifecycle policy in Azure Active Directory

## EXAMPLES

### Example 1
```
PS C:\>Add-AzureADMSLifecyclePolicyGroup -Id "b4c908b0-3595-4add-91b4-c5400b31b57b" -groupId "cffd97bd-6b91-4c4e-b553-6918a320211c"
```

This command adds a group to the lifecycle policy.

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

### -Id
Specifies the ID of the lifecycle policy object in Azure Active Directory.

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
