---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSPrivilegedRoleSetting

## SYNOPSIS
Update role setting

## SYNTAX

```
Set-AzureADMSPrivilegedRoleSetting -ProviderId <String> -Id <String> [-ResourceId <String>]
 [-RoleDefinitionId <String>]
 [-AdminEligibleSettings <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]>]
 [-AdminMemberSettings <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]>]
 [-UserEligibleSettings <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]>]
 [-UserMemberSettings <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]>]
 [<CommonParameters>]
```

## DESCRIPTION
Update role setting

## EXAMPLES

### Example 1
```
PS C:\> $setting = New-Object Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting
				  PS C:\> $setting.RuleIdentifier = "JustificationRule"
				  PS C:\> $setting.Setting = "{'required':false}"
				  PS C:\> Set-AzureADMSPrivilegedRoleSetting -ProviderId AzureResources -Id ff518d09-47f5-45a9-bb32-71916d9aeadf -ResourceId 3f5887ed-dd6e-4821-8bde-c813ec508cf9 -RoleDefinitionId 2387ced3-4e95-4c36-a915-73d803f93702 -UserMemberSettings $setting
```

Update a role setting by setting the justification to be false

## PARAMETERS

### -AdminEligibleSettings
The rule settings that are evaluated when an administrator tries to add an eligible role assignment.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdminMemberSettings
The rule settings that are evaluated when an administrator tries to add an activate role assignment.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
The unique identifier of the specific role setting

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

### -ProviderId
The unique identifier of the specific provider

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

### -ResourceId
The unique identifier of the specific resource

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
The unique identifier of the specific role definition

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserEligibleSettings
The rule settings that are evaluated when a user tries to add an eligible role assignment.
This is not supported for pimforazurerbac scenario for now, and may be available in the future scenarios.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserMemberSettings
The rule settings that are evaluated when a user tries to activate his role assignment.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AzureADMSPrivilegedRuleSetting]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
