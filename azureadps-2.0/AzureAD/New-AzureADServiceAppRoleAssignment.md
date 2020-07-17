---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 35D6752C-1503-412C-84D0-3775EC30CE13
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
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
The **New-AzureADServiceAppRoleAssignment** cmdlet assigns a service principal to an application role in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -Id
The role id that was assigned to the principal. This role must be declared by the target resource application resourceId in its appRoles property. Where the resource does not declare any permissions, a default id (zero GUID) must be specified.

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
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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
The ID of the user (as a UserPrincipalName or ObjectId) in Azure AD to be assigned to the app role.

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
The unique identifier (objectId) for the principal being granted the access.

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
The unique identifier (objectId) for the target resource (service principal) for which the assignment was made.

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

[Get-AzureADServiceAppRoleAssignment](./Get-AzureADServiceAppRoleAssignment.md)

[Remove-AzureADServiceAppRoleAssignment](./Remove-AzureADServiceAppRoleAssignment.md)
