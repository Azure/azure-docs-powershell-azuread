---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: AD722FB5-9280-479F-8CDA-2A4572FDCA4F
---

# Remove-MsolServicePrincipalCredential

## SYNOPSIS
Removes a credential key from a service principal.

## SYNTAX

### RemoveServicePrincipalCredentials__0 (Default)
```
Remove-MsolServicePrincipalCredential -ObjectId <Guid> -KeyIds <Guid[]> [-TenantId <Guid>] [<CommonParameters>]
```

### RemoveServicePrincipalCredentialsBySpn__0
```
Remove-MsolServicePrincipalCredential -KeyIds <Guid[]> -ServicePrincipalName <String> [-TenantId <Guid>]
 [<CommonParameters>]
```

### RemoveServicePrincipalCredentialsByAppPrincipalId__0
```
Remove-MsolServicePrincipalCredential -KeyIds <Guid[]> -AppPrincipalId <Guid> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolServicePrincipalCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.
The service principal is identified by supplying either the object ID, application ID, or service principal name (SPN).
The credential to be removed is identified by its key ID.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolServicePrincipalCredential -KeyIds @("19805a93-e9dd-4c63-8afd-88ed91f33546") -ServicePrincipalName "MyApp2/myApp.com"
```

Description

-----------

This command removes a credential key from a service principal.
In this example, the key ID "19805a93-e9dd-4c63-8afd-88ed91f33546" will be removed from the service principal associated with the service principal name "MyApp2/myApp.com".
To show a list of key IDs associated with a service principal, use the Get-MsolServicePrincipalCredential cmdlet.

## PARAMETERS

### -AppPrincipalId
The application ID associated with the service principal to remove the credential from.

```yaml
Type: Guid
Parameter Sets: RemoveServicePrincipalCredentialsByAppPrincipalId__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyIds
Specifies the list of credential keys to be removed.
The list of key IDs for a service principal can be obtained using the Get-MsolServicePrincipalCredential cmdlet.

```yaml
Type: Guid[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The object ID of the service principal to remove the credential from.

```yaml
Type: Guid
Parameter Sets: RemoveServicePrincipalCredentials__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
The unique name of the service principal to add the credential to.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL. 
AppName represents the name of the application and hostname represents the URI authority for the application.

```yaml
Type: String
Parameter Sets: RemoveServicePrincipalCredentialsBySpn__0
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


