---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 3F9E2B81-398B-4C87-B786-DF5C59FAE369
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolServicePrincipal

## SYNOPSIS
Gets service principals from Azure Active Directory.

## SYNTAX

### ListServicePrincipals__0 (Default)
```
Get-MsolServicePrincipal [-SearchString <String>] [-MaxResults <Int32>] [-TenantId <Guid>] [<CommonParameters>]
```

### GetServicePrincipal__0
```
Get-MsolServicePrincipal -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### GetServicePrincipalByAppPrincipalId__0
```
Get-MsolServicePrincipal -AppPrincipalId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### GetServicePrincipalBySpn__0
```
Get-MsolServicePrincipal -ServicePrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolServicePrincipal [-SearchString <String>] [-All] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolServicePrincipal** cmdlet gets a service principal or a list of service principals from Azure Active Directory.

## EXAMPLES

### Example 1: Display all service principals
```
PS C:\> Get-MsolServicePrincipal
```

This command displays all the existing service principals in the organization's tenant.

### Example 2: Get service principals by using a name
```
PS C:\> Get-MsolServicePrincipal -ServicePrincipalName "MyApp"
```

This command gets all the existing service principals that have a service principal name that starts with MyApp.
This is an exact match of the **appClass** portion of the service principal name up to the forward slash.

### Example 3: Get a service principal
```
PS C:\> Get-MsolServicePrincipal -AppPrincipalId 5e964d2f-e384-4292-ae55-dd24c89cc53b
```

This command gets a service principal that has a specific application principal ID.

## PARAMETERS

### -All
Indicates that this cmdlet returns all results.
Do not specify together with the _MaxResults_ parameter.

```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppPrincipalId
Specifies the unique application ID of the service principal to get.

```yaml
Type: Guid
Parameter Sets: GetServicePrincipalByAppPrincipalId__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.
The default value is 500.

```yaml
Type: Int32
Parameter Sets: ListServicePrincipals__0
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the service principal to get.

```yaml
Type: Guid
Parameter Sets: GetServicePrincipal__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Specifies the name of the service principal or service principals to get.
An SPN must use one of the following formats:

* `appName`
* `appName/hostname`
* a valid URL

AppName represents the name of the application and hostname represents the URI authority for the application.
```yaml
Type: String
Parameter Sets: GetServicePrincipalBySpn__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
Specifies a string to match service principal names.


```yaml
Type: String
Parameter Sets: ListServicePrincipals__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.ServicePrincipal[]
This cmdlet returns a service principal or a list of service principals from Azure Active Directory.
Each service principal contains the following information:

* ObjectId. The unique identifier of the service principal.
* AppPrincipalId. The application identifier of the service principal.
* DisplayName. The friendly name of the service principal.
* ServicePrincipalName. The list of service principal names (SPNs) associated with the service principal.
* AccountEnabled. The value indicating if the account is enabled.

## NOTES

## RELATED LINKS
[New-MsolServicePrincipal](./New-MsolServicePrincipal.md)

[Remove-MsolServicePrincipal](./Remove-MsolServicePrincipal.md)

[Set-MsolServicePrincipal](./Set-MsolServicePrincipal.md)
