---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 67573FFF-F6B6-4681-A96C-05BB5874F9FB
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-MsolServicePrincipalCredential

## SYNOPSIS
Add a credential key to a service principal.

## SYNTAX

### AddServicePrincipalCredentials__0 (Default)
```
New-MsolServicePrincipalCredential -ObjectId <Guid> [-Type <ServicePrincipalCredentialType>] [-Value <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Usage <ServicePrincipalCredentialUsage>] [-TenantId <Guid>]
 [<CommonParameters>]
```

### AddServicePrincipalCredentialsBySpn__0
```
New-MsolServicePrincipalCredential -ServicePrincipalName <String> [-Type <ServicePrincipalCredentialType>]
 [-Value <String>] [-StartDate <DateTime>] [-EndDate <DateTime>] [-Usage <ServicePrincipalCredentialUsage>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### AddServicePrincipalCredentialsByAppPrincipalId__0
```
New-MsolServicePrincipalCredential -AppPrincipalId <Guid> [-Type <ServicePrincipalCredentialType>]
 [-Value <String>] [-StartDate <DateTime>] [-EndDate <DateTime>] [-Usage <ServicePrincipalCredentialUsage>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MsolServicePrincipalCredential** cmdlet adds a new credential to a service principal or adds or rolls credential keys for an application.
The service principal is identified by supplying either the object ID, app principal ID, or service principal name (SPN).

## EXAMPLES

### Example 1: Add a credential to a service principal
```
PS C:\> New-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com"
```

This command adds a credential, or a key, object to an existing service principal.
In this example, a symmetric key is generated for this credential and added to the service principal using the service principal name value of MyApp/myApp.com.

### Example 2: Add an existing credential to a service principal
```
PS C:\> $Certificate = New-Object System.Security.Cryptography.X509Certificates.X509Certificate
PS C:\> $Certificate.Import("C:\myapp.cer")
PS C:\> $BinCert = $Certificate.GetRawCertData()
PS C:\> $CredValue = [System.Convert]::ToBase64String($binCert);
PS C:\> New-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com" -Type asymmetric -Value $CredValue -StartDate $Certificate.GetEffectiveDateString() -EndDate $Certificate.GetExpirationDateString()
```

This example adds a credential, or a key, object to an existing service principal.
In this example, the supplied base64 encoded public X509 certificate, named myapp.cer, is added to the service principal using the service principal name value of MyApp/myApp.com.

### Example 3: Register an on-premises Exchange Server
```
PS C:\> New-MsolServicePrincipalCredential -AppPrincipalId  -Type asymmetric -Value $CredValue
```

This command registers an on-premises Exchange Server so that communications between the Exchange Server and Microsoft Azure Active Directory services such as Office 365 can occur.
This example assumes that $credValue contains the base64 encoded public X509 certificate used to represent the on-premises Exchange server.
The well known IDs for Office 365 servers are:

* Exchange: 00000002-0000-0ff1-ce00-000000000000
* SharePoint: 00000003-0000-0ff1-ce00-000000000000
* Lync: 00000004-0000-0ff1-ce00-000000000000

## PARAMETERS

### -AppPrincipalId
Specifies the application ID of the service principal to which to add the credential.

```yaml
Type: Guid
Parameter Sets: AddServicePrincipalCredentialsByAppPrincipalId__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndDate
Specifies the effective end date of the credential usage.
The default value is one year from today.
For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid until, otherwise an OAuth token will not be issued for this application.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Today + 1 year
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the service principal to which to add the credential.

```yaml
Type: Guid
Parameter Sets: AddServicePrincipalCredentials__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Specifies the name of the service principal to which to add the credential.
An SPN must use one of the following formats:

* `appName`
* `appName/hostname`
* a valid URL

AppName represents the name of the application.
Hostname represents the URI authority for the application.

```yaml
Type: String
Parameter Sets: AddServicePrincipalCredentialsBySpn__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDate
Specifies the effective start date of the credential usage.
The default value is today.
For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from, otherwise an OAuth token will not be issued for this application.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Today
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

### -Type
Specifies the type of credential used.
Valid values are:

* asymmetric
* symmetric
* password

The default value is symmetric.

```yaml
Type: ServicePrincipalCredentialType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Symmetric
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Usage
Specifies the usage of the credential key.
The credential key usage can either be set to sign or verify a token.
The default value is verify.
Sign is allowed ONLY for symmetric keys.
Verify is allowed for all key types.

A verify credential key is required by the Azure Active Directory directory to verify that the request token was sent by your application, which is represented by this service principal.

Your application may optionally require that Azure Active Directory services issue tokens to your application signed with your signing key rather than the asymmetric public key identifying Microsoft Azure Active Directory.
In this case, provide a sign credential key for your service principal.

```yaml
Type: ServicePrincipalCredentialUsage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Verify
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Specifies the value of the credential.

* If the credential type is asymmetric, the value represents the base 64 encoded certificate.
* If the credential type is symmetric and the _Value_ parameter is not specified, a 256 bit AES key is automatically created and valid for one year from creation.
* If the credential type is password, specify _Value_.
It should not be base 64 encoded.

```yaml
Type: String
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

[Remove-MsolServicePrincipalCredential](./Remove-MsolServicePrincipalCredential.md)
