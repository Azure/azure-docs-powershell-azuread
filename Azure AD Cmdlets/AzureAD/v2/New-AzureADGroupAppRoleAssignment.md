---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: B2EE39EC-3CD7-4F55-8D27-9E32E4E152C3
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-AzureADGroupAppRoleAssignment

## SYNOPSIS
Assigns a group to an application role.

## SYNTAX

```
New-AzureADGroupAppRoleAssignment -ObjectId <String> -PrincipalId <String> -ResourceId <String> -Id <String>
[-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADGroupAppRoleAssignment** cmdlet assigns a group to an application role in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Assign a group to an application without roles

This example assigns a group to an application that doesn't have any app roles defined, using the default app role ID.

```PowerShell
# Get the service principal of the app to assign the group to
$servicePrincipal = Get-AzureADServicePrincipal -SearchString "<Your app's display name>"

# Get the group to be assigned
$group = Get-AzureADGroup -SearchString "<Your group's name>"

# Create the group app role assignment
New-AzureADGroupAppRoleAssignment -ObjectId $group.ObjectId -PrincipalId $group.ObjectId -ResourceId $servicePrincipal.ObjectId -Id ([Guid]::Empty)
```

### Example 2: Assign a group to a specific app role within an application

This example assigns the specified group to a given app role. Please refer to the description of the `-Id` parameter for more information on how to retrieve application roles for an application.

```PowerShell
$group_name = "<You group's name>"
$app_name = "<Your App's display name>"
$app_role_name = "<App role display name>"

# Get the group to assign, and the service principal for the app to assign to
$group = Get-AzureADGroup -SearchString "$group_name"
$sp = Get-AzureADServicePrincipal -Filter "displayName eq '$app_name'"
$appRole = $sp.AppRoles | Where-Object { $_.DisplayName -eq $app_role_name }

# Assign the group to the app role
New-AzureADGroupAppRoleAssignment -ObjectId $group.ObjectId -PrincipalId $group.ObjectId -ResourceId $sp.ObjectId -Id $appRole.Id
```

## PARAMETERS

### -ObjectId
The object ID of the group in Azure AD to be assigned to the app role.

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
The object ID of the principal which will be assigned to the app role. When assigning a group to an app role, provide the object ID of the group.

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
The object ID of the ServicePrincipal for the application for which the group is being assigned an app role.

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
The ID of the app role to assign. Provide an empty Guid (`[Guid]::Empty`) when creating an app role assignement for an application that does not have any app roles defined, or the `Id` of the app role to assign the group to.

You can retrieve the application's app roles by examining the application object's AppRoles property:

```Powershell
Get-AzureADServicePrincipal -SearchString "Your Application display name" | Format-List AppRoles 
```

This cmdlet returns the list of roles that are defined in an application:

```
AppRoles : {class AppRole {
            AllowedMemberTypes: System.Collections.Generic.List1[System.String]
            Description: <description for this role>
            DisplayName: <display name for this role>
            Id: 97e244a2-6ccd-4312-9de6-ecb21884c9f7
            IsEnabled: True
            Value: <Value that will be transmitted as a claim in a token for this role>
        }
        }
```

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADGroupAppRoleAssignment](./Get-AzureADGroupAppRoleAssignment.md)

[Remove-AzureADGroupAppRoleAssignment](./Remove-AzureADGroupAppRoleAssignment.md)

