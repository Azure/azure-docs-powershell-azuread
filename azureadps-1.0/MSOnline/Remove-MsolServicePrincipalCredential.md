---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: AD722FB5-9280-479F-8CDA-2A4572FDCA4F
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
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
The **Remove-MsolServicePrincipalCredential** cmdlet removes a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.
The service principal is identified by supplying either the object ID, application ID, or service principal name (SPN).
The credential to be removed is identified by its key ID.

## EXAMPLES

### Example 1: Remove a credential from a service principal
```
PS C:\> Remove-MsolServicePrincipalCredential -KeyIds @("19805a93-e9dd-4c63-8afd-88ed91f33546") -ServicePrincipalName "MyApp2/myApp.com"
```

This command removes a credential key from a service principal.
In this example, the key ID 19805a93-e9dd-4c63-8afd-88ed91f33546 is removed from the service principal associated with the service principal name MyApp2/myApp.com.
To show a list of key IDs associated with a service principal, use the [Get-MsolServicePrincipalCredential](./Get-MsolServicePrincipalCredential.md) cmdlet.

## PARAMETERS

### -AppPrincipalId
Specifies the application ID of the service principal from which to remove the credential.

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
Specifies an array of unique IDs of credential keys to remove.
The key IDs for a service principal can be obtained by using the [Get-MsolServicePrincipalCredential](./Get-MsolServicePrincipalCredential.md) cmdlet.

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
Specifies the unique object ID of the service principal from which to remove the credential.

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
Specifies the name of the service principal from which to remove the credential.
An SPN must use one of the following formats:

* `appName`
* `appName/hostname`
* a valid URL

AppName represents the name of the application.
Hostname represents the URI authority for the application.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[Get-MsolServicePrincipalCredential](./Get-MsolServicePrincipalCredential.md)

[New-MsolServicePrincipalCredential](./New-MsolServicePrincipalCredential.md)
