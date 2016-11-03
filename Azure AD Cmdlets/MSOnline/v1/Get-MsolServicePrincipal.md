---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 3F9E2B81-398B-4C87-B786-DF5C59FAE369
---

# Get-MsolServicePrincipal

## SYNOPSIS
Retrieves a service principal or list of service principals from Microsoft Azure Active Directory.

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
The Get-MsolServicePrincipal cmdlet can be used to retrieve a service principal or a list of service principals from Microsoft Azure Active Directory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolServicePrincipal -ServicePrincipalName "

          Returns a list of service principals
```

Description

-----------

This command will list all of the existing service principals in the organization's tenant.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MsolServicePrincipal -ServicePrincipalName "MyApp"

          Returns a list of service principals.
```

Description

-----------

This command lists all of the existing service principals that have a ServicePrincipalName that start with "MyApp".
Note: This is an exact match of the appClass portion of the ServicePrincipalName up to the forward slash.

### -------------------------- EXAMPLE 3 --------------------------
```
Get-MsolServicePrincipal -AppPrincipalId 5e964d2f-e384-4292-ae55-dd24c89cc53b

          Returns a service principal.
```

Description

-----------

This command gets a service principal with a specific AppPrincipalId.
In this example, the value of "5e964d2f-e384-4292-ae55-dd24c89cc53b" might return a service principal named "MyApp3".

## PARAMETERS

### -All
If present then all results will be returned.
Cannot be used with the MaxResults parameter.

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
The application ID associated with the service principal to retrieve.

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
The maximum number of results returned for a search result.
If not specified, 500 results will be returned.

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
The object ID associated with the service principal to retrieve.

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
The unique name of the service principal to retrieve.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL. 
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
The unique ID of the tenant to perform the operation on.
If this is not provided, then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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
Retrieve a service principal or a list of service principals from Microsoft Azure Active Directory.
Each service principal contains the following information:

            ObjectId - The unique identifier of the service principal.
            AppPrincipalId - The application identifier of the service principal.
            DisplayName - The friendly name of the service principal.
            ServicePrincipalName - The list of service principal names (SPNs) associated with the service principal.
            AccountEnabled - The value indicating if the account is enabled.

## NOTES

## RELATED LINKS


