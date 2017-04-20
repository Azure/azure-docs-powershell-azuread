---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 3B666786-2620-4E80-9A36-552B942A9F7C
online version: 
schema: 2.0.0
---

# New-AzureADUserAppRoleAssignment

## SYNOPSIS
Assigns a user to an application role.

## SYNTAX

```
New-AzureADUserAppRoleAssignment -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] -Id <String> -PrincipalId <String> -ResourceId <String> [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADUserAppRoleAssignment** cmdlet assigns a user to an application role in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Assign a user to an application without roles
```
# Get AppId of the app to assign the user to

$appId = Get-AzureADApplication -SearchString â€œ<Your App's display name>â€

# Get the user to be added

$user = Get-AzureADUser -searchstring "<Your user's UPN>"

# Get the service principal for the app you want to assign the user to

$servicePrincipal = Get-AzureADServicePrincipal -Filter â€œappId eq â€˜$appId'â€

# Create the user app role assignment

New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $servicePrincipal.ObjectId -Id ([Guid]::Empty)
```

This command assigns a user to and application that doesn;t have any roles.

### Example 2: Assign a user to a specific role within an application
```
$username = "<You user's UPN>"
$appname = "<Your App's display name>"
$spo = Get-AzureADServicePrincipal -Filter "Displayname eq '$appname'"
$user = Get-AzureADUser -ObjectId $username
New-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -PrincipalId $user.ObjectId -ResourceId $spo.ObjectId -Id $spo.Approles[1].id
```

This cmdlet assigns to the specified user the application role of which the Id is specified with $spo.Approles[1].id. please refer to the description of the -Id parameter for more information on how to retrieve application roles for an application.

## PARAMETERS

### -Id
The ID of the app role to assign. Provide an empty guid when creating a new app role assignement for an application that does not have any roles, or the Id of the role to assign to the user.

You can retrieve the application's roles by examining the application object's AppRoles property:

	Get-AzureadApplication -SearchString "Your Application display name" | select Approles | Fl 

This cmdlet returns the list of roles that are defined in an application:

	AppRoles : {class AppRole {
             AllowedMemberTypes: System.Collections.Generic.List1[System.String]
             Description: <description for this role>
             DisplayName: <display name for this role>
             Id: 97e244a2-6ccd-4312-9de6-ecb21884c9f7
             IsEnabled: True
             Value: <Value that will be transmitted as a claim in a token for this role>
           }
           }


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
Specifies the ID of the user (as a UPN or ObjectId) in Azure AD to which the new app role is to be assigned

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
The object ID of the principal to which the new app role is assigned. When assigning a new role to a user provide the object ID of the user.

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
The object ID of the Service Principal for the application to which the user role is assigned.

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

[Get-AzureADUserAppRoleAssignment](./Get-AzureADUserAppRoleAssignment.md)

[Remove-AzureADUserAppRoleAssignment](./Remove-AzureADUserAppRoleAssignment.md)
