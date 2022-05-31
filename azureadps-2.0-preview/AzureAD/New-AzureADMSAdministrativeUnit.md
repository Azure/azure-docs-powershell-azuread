---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSAdministrativeUnit

## SYNOPSIS
Creates an administrative unit.

## SYNTAX

```
New-AzureADMSAdministrativeUnit [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-Description <String>] -DisplayName <String> [-IsMemberManagementRestricted <Boolean>]
 [-MembershipRule <String>] [-MembershipRuleProcessingState <String>] [-MembershipType <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSAdministrativeUnit cmdlet creates an administrative unit in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> $adminUnit = New-AzureADMSAdministrativeUnit -DisplayName "Example Admin Unit" -Description "An example of an administrative unit" -MembershipType "Dynamic" -MembershipRuleProcessingState "On" -MembershipRule '(user.country -eq "United States")'
```

Creates a new administrative unit called Example Admin Unit with a dynamic membership rule to include all users in the United States.

## PARAMETERS

### -Description
Specifies a description for the new administrative unit.

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

### -DisplayName
Specifies the display name of the new administrative unit.

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

### -IsMemberManagementRestricted
Indicates whether the management rights on resources in the administrative units should be restricted to ONLY the administrators scoped on the AU object.
If no value is specified, it will default to false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MembershipRule
Specifies the membership rule for a dynamic administrative unit.

For more information about the rules that you can use for dynamic administrative units and dynamic groups, see [Using attributes to create advanced rules](https://azure.microsoft.com/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

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

### -MembershipRuleProcessingState
Specifies the rule processing state. The acceptable values for this parameter are:

- "On". Process the group rule.
- "Paused". Stop processing the group rule.

Changing the value of the processing state does not change the members list of the administrative unit.


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

### -MembershipType
Specifies whether the membership of this administrative unit is controlled dynamically or by manual assignment.
The acceptable values for this parameter are:

- Assigned
- Dynamic

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADMSAdministrativeUnit](https://docs.microsoft.com/powershell/module/azuread/get-azureadmsadministrativeunit?view=azureadps-2.0-preview)

[Remove-AzureADMSAdministrativeUnit](https://docs.microsoft.com/powershell/module/azuread/remove-azureadadministrativeunit?view=azureadps-2.0-preview)

[Set-AzureADMSAdministrativeUnit](https://docs.microsoft.com/powershell/module/azuread/set-azureadmsadministrativeunit?view=azureadps-2.0-preview)
