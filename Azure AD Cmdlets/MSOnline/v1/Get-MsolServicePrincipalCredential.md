---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 171F9F72-AD52-48CF-9E6E-553EEDD6B2D3
---

# Get-MsolServicePrincipalCredential

## SYNOPSIS
Retrieves a list of credentials associated with a service principal.

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
The Get-MsolServicePrincipalCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.

## EXAMPLES

### Example 1:
```
PS C:\> Get-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com"

          Returns a list of credentials associated with the "MyApp/myApp.com" service principal.
```

Description

-----------

This command will retrieve all of the credential properties (but not the credential value) associated with the service principal name (SPN) "MyApp/myApp.com".
An SPN must follow the format appClass/hostname, where appClass represents the application class ("MyApp") and hostname represents the hostname for the application (myApp.com).

## PARAMETERS

### -AppPrincipalId
The application ID associated with the service principal credentials to retrieve.

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
The object ID associated with the service principal credentials to retrieve.

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
The unique name of the service principal to retrieve credentials from.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL.
AppName represents the name of the application and hostname represents the URI authority for the application.

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

### -ReturnKeyValues


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
Retrieves the list of credentials associated with a service principal.
Each service principal contains the following information:

            Type - The type of service principal credential (Asymmetric/Symmetric/Password).
            Value - The value of the credential.
If the credential type is certificate, this represents the base 64 encoded certificate.
If credential type is symmetric, it represents an AES key.
            KeyGroupId - The identifier reserved for internal use.
            KeyId - The unique identifier of the key.
            StartDate - The effective start date of the credential usage.
            EndDate - The effective end date of the credential usage.
            Usage  - Specifies if the credential is used to "sign" or "verify" a token.

## NOTES

## RELATED LINKS
