---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: B2EE39EC-3CD7-4F55-8D27-9E32E4E152C3
online version: 
schema: 2.0.0
---

# New-AzureADGroupAppRoleAssignment

## SYNOPSIS
Assign a group of users to an application role.

## SYNTAX

```
New-AzureADGroupAppRoleAssignment -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] -Id <String> -PrincipalId <String> -ResourceId <String> [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADGroupAppRoleAssignment** cmdlet assigns a group of users to an application role in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -Id
Specifies the ID.

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

### -ObjectId
Specifies the ID of a user (as a UPN or ObjectId) in Azure AD.

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

### -PrincipalId
Specifies the principal ID.

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

### -ResourceId
Specifies the resource ID.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADGroupAppRoleAssignment](./Get-AzureADGroupAppRoleAssignment.md)

[Remove-AzureADGroupAppRoleAssignment](./Remove-AzureADGroupAppRoleAssignment.md)

[Managing applications in Azure Active Directory using PowerShell](https://channel9.msdn.com/Series/Azure-Active-Directory-Videos-Demos/ManageAppsAzureADPowerShell) 
