---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADServiceAppRoleAssignment

## SYNOPSIS
Assigns a service principal to an application role.

## SYNTAX

```
New-AzureADServiceAppRoleAssignment -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] -Id <String> -PrincipalId <String> -ResourceId <String> [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADServiceAppRoleAssignment cmdlet assigns a service principal to an application role in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> New-AzureADServiceAppRoleAssignment -ObjectID 'd2d32a8c-0330-4d09-9509-928fe8fa80a2' -Id '584a9c48-9bae-444f-9116-f12d464ae1fc' -PrincipalID 'd2d32a8c-0330-4d09-9509-928fe8fa80a2' -ResourceID '5bb2f317-c13d-4721-afc4-e4be996eb43f'
```

In this example,

- `ObjectId`:  The Id of the client service principal to which you are assigning the app role.
- `Id`: The Id of the appRole (defined on the resource service principal) to assign to the client service principal.
- `PrincipalId`: The Id of the client service principal to which you are assigning the app role.
- `ResourceId`: The Id of the resource servicePrincipal which has defined the app role.

## PARAMETERS

### -Id
Specifies the Id of the appRole (defined on the resource service principal) to assign to the client service principal.

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
Specifies the Id of the client service principal to which you are assigning the app role.

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
Specifies the Id of the client service principal to which you are assigning the app role.

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
Specifies the Id of the Service Principal which has defined the app role..

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServiceAppRoleAssignment]()

[Remove-AzureADServiceAppRoleAssignment]()

