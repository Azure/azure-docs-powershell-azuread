---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 87A60137-58ED-473B-9D1E-BB7C0CD8F8A2
---

# Remove-MsolServicePrincipal

## SYNOPSIS
Removes a service principal from Microsoft Azure Active Directory.

## SYNTAX

### RemoveServicePrincipal__0 (Default)
```
Remove-MsolServicePrincipal -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveServicePrincipalByAppPrincipalId__0
```
Remove-MsolServicePrincipal -AppPrincipalId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveServicePrincipalBySpn__0
```
Remove-MsolServicePrincipal -ServicePrincipalName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolServicePrincipal cmdlet removes a service principal from Microsoft Azure Active Directory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolServicePrincipal -ServicePrincipalName "MyApp/myApp.com"
```

Description

-----------

This command removes a service principal by specifying one of its service principal names.
In this example, the service principal associated with the service principal name "MyApp/myApp.com" would be removed.

## PARAMETERS

### -AppPrincipalId
The unique application identifier associated with the service principal to be removed.

```yaml
Type: Guid
Parameter Sets: RemoveServicePrincipalByAppPrincipalId__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The object ID of the service principal to be removed.

```yaml
Type: Guid
Parameter Sets: RemoveServicePrincipal__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
The unique name of the service principal or service principals to be removed.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL. 
AppName represents the name of the application and hostname represents the URI authority for the application.

```yaml
Type: String
Parameter Sets: RemoveServicePrincipalBySpn__0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


