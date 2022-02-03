---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADServiceAppRoleAssignment

## SYNOPSIS
Assigns an app role to a user, a group, or another service principal.

## SYNTAX

```
New-AzureADServiceAppRoleAssignment -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] -Id <String> -PrincipalId <String> -ResourceId <String> [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADServiceAppRoleAssignment cmdlet assigns an app role from a resource service principal to a user, a group, or another service principal. App roles assigned to service principals are also known as application permissions.

> [!NOTE]
> The behavior described here applies when `Connect-AzureAD` was called without any parameters, or using a Microsoft-owned application identity. See [Example 4](#example-4-when-connected-using-a-customer-owned-app-or-service-identity) to learn more about the difference when connected using a customer-owned app registration or service identity.  

## EXAMPLES

### Example 1: Assign an app role to another service principal

```powershell
PS C:\> Connect-AzureAD
PS C:\> New-AzureADServiceAppRoleAssignment -ObjectId $resource.ObjectId -ResourceId $resource.ObjectId -Id $appRole.Id -PrincipalId $client.ObjectId
```

In this example, a client service principal is assigned an app role (application permission) defined by a resource service principal (for example, an API):

- `ObjectId`:  The ObjectId of the resource service principal (for example, an API).
- `ResourceId`: The ObjectId of the resource service principal (for example, an API).
- `Id`: The Id of the app role (defined on the resource service principal) to assign to the client service principal. If no app roles have been defined on the resource app, you can use `00000000-0000-0000-0000-000000000000`.
- `PrincipalId`: The ObjectId of the client service principal to which you are assigning the app role.

> [!NOTE]
> This example applies when `Connect-AzureAD` was called without any parameters. See [Example 4](#example-4--when-connected-using-a-customer-owned-app-or-service-identity) to see how this cmdlet is used when connected using a customer-owned app registration or service identity.

### Example 2: Assign an app role to a user

```powershell
PS C:\> Connect-AzureAD
PS C:\> New-AzureADServiceAppRoleAssignment -ObjectId $resource.ObjectId -ResourceId $resource.ObjectId -Id $appRole.Id -PrincipalId $user.ObjectId
```

In this example, a user is assigned an app role defined by a resource app:

- `ObjectId`:  The ObjectId of the app's service principal.
- `ResourceId`: The ObjectId of the app's service principal.
- `Id`: The Id of the app role (defined on the app's service principal) to assign to the user. If no app roles have been defined to the resource app, you can use `00000000-0000-0000-0000-000000000000` to indicate that the app is assigned to the user.
- `PrincipalId`: The ObjectId of the user to which you are assigning the app role.

> [!NOTE]
> This example applies when `Connect-AzureAD` was called without any parameters. See [Example 4](#example-4-when-connected-using-a-customer-owned-app-or-service-identity) to see how this cmdlet is used when connected using a customer-owned app registration or service identity. 

### Example 3: Assign an app role to a group

```powershell
PS C:\> Connect-AzureAD
PS C:\> New-AzureADServiceAppRoleAssignment -ObjectId $resource.ObjectId -ResourceId $resource.ObjectId -Id $appRole.Id -PrincipalId $group.ObjectId
```

In this example, a group is assigned an app role defined by a resource app. All users who are direct member of the assigned group are considered to be assigned the app role:

- `ObjectId`:  The ObjectId of the app's service principal.
- `ResourceId`: The ObjectId of the app's service principal.
- `Id`: The Id of the app role (defined on the app's service principal) to assign to the group. If no app roles have been defined on the resource app, you can use `00000000-0000-0000-0000-000000000000` to indicate the app is assigned to the group.
- `PrincipalId`: The ObjectId of the group to which you are assigning the app role.

> [!NOTE]
> This example applies when `Connect-AzureAD` was called without any parameters. See [Example 4](#example-4-when-connected-using-a-customer-owned-app-or-service-identity) to see how this cmdlet is used when connected using a customer-owned app registration or service identity. 

### Example 4: When connected using a customer-owned app or service identity

```powershell
PS C:\> Connect-AzureAD -TenantId $tenantOrDomain -ApplicationId $appId -CertificateThumbprint $thumb
PS C:\> New-AzureADServiceAppRoleAssignment -ObjectId $client.ObjectId -ResourceId $resource.ObjectId -Id $appRole.Id -PrincipalId $client.ObjectId
```

This cmdlet's behavior changes when connected to the Azure AD PowerShell module using a customer-owned app registration or service identity, including:

- When [connecting as a service principal](../../azureadps-2.0-preview/AzureAD/Connect-AzureAD.md#example-3-connect-a-session-as-a-service-principal), and
- When using the `AadAccessToken` parameter with an access token obtained for a customer-owned app registration or service identity.

Under these circumstances, this cmdlet is only used for assigning an app role to another service principal, identified by the `ObjectId` and `PrincipalId` parameters:

- `ObjectId`:  The ObjectId of the client service principal to which you are assigning the app role.
- `ResourceId`: The ObjectId of the resource service principal (for example, an API).
- `Id`: The Id of the app role (defined on the resource service principal) to assign to the client service principal. If no app roles have been defined on the resource app, you can use `00000000-0000-0000-0000-000000000000`.
- `PrincipalId`: The ObjectId of the client service principal to which you are assigning the app role.

When connected using a customer-owned app or service identity, use [New-AzureADUserAppRoleAssignment](New-AzureADUserAppRoleAssignment.md) and [New-AzureADGroupAppRoleAssignment](New-AzureADUserAppRoleAssignment.md) to create app role assignments for a user and groups, respectively.

## PARAMETERS

### -Id
Specifies the Id of the app role (defined on the resource service principal) to assign. If no app roles have been defined on the resource app, you can use `00000000-0000-0000-0000-000000000000` to indicate assignment of the resource app or service, without specifying an app role.

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
Specifies the ObjectId of the resource service principal (such as an app or an API) that is going to be assigned to a user, a group, or another service principal.

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
Specifies the ObjectId of the user, group, or other service principal to which the app role is being assigned.

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
Specifies the ObjectId of the resource service principal (such as an app or an API) that is going to be assigned to a user, a group, or another service principal.

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

