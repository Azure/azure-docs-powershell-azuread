---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 171F9F72-AD52-48CF-9E6E-553EEDD6B2D3
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolServicePrincipalCredential

## SYNOPSIS
Gets credentials associated with a service principal.

## SYNTAX

### ListServicePrincipalCredentials__0 (Default)
```
Get-MsolServicePrincipalCredential -ObjectId <Guid> -ReturnKeyValues <Boolean> [-TenantId <Guid>]
 [<CommonParameters>]
```

### ListServicePrincipalCredentialsByAppPrincipalId__0
```
Get-MsolServicePrincipalCredential -ReturnKeyValues <Boolean> -AppPrincipalId <Guid> [-TenantId <Guid>]
 [<CommonParameters>]
```

### ListServicePrincipalCredentialsBySpn__0
```
Get-MsolServicePrincipalCredential -ReturnKeyValues <Boolean> -ServicePrincipalName <String> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolServicePrincipalCredential** cmdlet gets credentials that are associated with a service principal.

## EXAMPLES

### Example 1: Get credential properties
```
PS C:\> Get-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com"
```

This command gets all the credential properties, except the credential value, that are associated with the service principal name (SPN) MyApp/myApp.com.
An SPN must follow the format appClass/hostname, where appClass represents the application class ("MyApp") and hostname represents the hostname for the application (myApp.com).

## PARAMETERS

### -AppPrincipalId
Specifies the application ID of the service principal for which to get credentials.

```yaml
Type: Guid
Parameter Sets: ListServicePrincipalCredentialsByAppPrincipalId__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the service principal for which to get credentials.

```yaml
Type: Guid
Parameter Sets: ListServicePrincipalCredentials__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Specifies the name of the service principal from which to get credentials.
An SPN must use one of the following formats:

* `appName`
* `appName/hostname`
* a valid URL

AppName represents the name of the application.
Hostname represents the URI authority for the application.

```yaml
Type: String
Parameter Sets: ListServicePrincipalCredentialsBySpn__0
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

### -ReturnKeyValues
Indicates whether this cmdlet returns key values.


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.ServicePrincipalCredential[]
This cmdlet returns the credentials that are associated with a service principal.
Each returned object contains the following information:

* Type. The type of service principal credential (Asymmetric/Symmetric/Password).
* Value. The value of the credential.
  * If the credential type is certificate, this represents the base 64 encoded certificate.
  * If credential type is symmetric, it represents an AES key.
* KeyGroupId. The identifier reserved for internal use.
* KeyId. The unique identifier of the key.
* StartDate. The effective start date of the credential usage.
* EndDate. The effective end date of the credential usage.
* Usage . Specifies if the credential is used to "sign" or "verify" a token.

## NOTES

## RELATED LINKS
[New-MsolServicePrincipalCredential](./New-MsolServicePrincipalCredential.md)

[Remove-MsolServicePrincipalCredential](./Remove-MsolServicePrincipalCredential.md)
