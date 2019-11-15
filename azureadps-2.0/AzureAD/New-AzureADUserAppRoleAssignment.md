---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 3B666786-2620-4E80-9A36-552B942A9F7C
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-AzureADUserAppRoleAssignment

## SYNOPSIS
Assigns a user to an application role.

## SYNTAX

```
New-AzureADUserAppRoleAssignment -ObjectId <String> -PrincipalId <String> -ResourceId <String> -Id <String>
[-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADUserAppRoleAssignment** cmdlet assigns a user to an application role in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Assign a user to an application without roles

This example assigns a user to an application that doesn't have any app roles defined, using the default app role ID.

```
# Get the service principal of the app to assign the user to
$servicePrincipal = Get-AzureADServicePrincipal -SearchString "<Your app's display name>"

# Get the user to be assigned
$user = Get-AzureADUser -searchstring "<Your user's UPN>"

# Create the user app role assignment
New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $servicePrincipal.ObjectId -Id ([Guid]::Empty)
```

### Example 2: Assign a user to a specific app role within an application

This example assigns the specified user the to a given app role. Please refer to the description of the `-Id` parameter for more information on how to retrieve application roles for an application.

```PowerShell
$username = "<You user's UPN>"
$app_name = "<Your App's display name>"
$app_role_name = "<App role display name>"

# Get the user to assign, and the service principal for the app to assign to
$user = Get-AzureADUser -ObjectId "$username"
$sp = Get-AzureADServicePrincipal -Filter "displayName eq '$app_name'"
$appRole = $sp.AppRoles | Where-Object { $_.DisplayName -eq $app_role_name }

#Assign the user to the app role
New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $sp.ObjectId -Id $appRole.Id
```


## PARAMETERS

### -ObjectId
The ID of the user (as a `UserPrincipalName` or `ObjectId`) in Azure AD to be assigned to the app role.

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
The object ID of the principal to which the new app role is assigned. When assigning a user to an app role, provide the object ID of the user.

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
The object ID of the ServicePrincipal for the application for which the user is being assigned an app role.

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
The ID of the app role to assign. Provide an empty Guid (`[Guid]::Empty`) when creating an app role assignment for an application that does not have any app roles defined, or the `Id` of the app role to assign the user to.

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

[Get-AzureADUserAppRoleAssignment](./Get-AzureADUserAppRoleAssignment.md)

[Remove-AzureADUserAppRoleAssignment](./Remove-AzureADUserAppRoleAssignment.md)
