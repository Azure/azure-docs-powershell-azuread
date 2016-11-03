---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 67573FFF-F6B6-4681-A96C-05BB5874F9FB
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
The New-MsolServicePrincipalCredential cmdlet can be used to add a new credential to a service principal or to add or roll credential keys for an application.
The service principal is identified by supplying either the object ID, appPrincipalID, or service principal name (SPN).

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
New-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com"

          New credential object added, including the symmteric key generated and the KeyId for the added credential.
```

Description

-----------

This command adds a credential (or a key) object to an existing service principal.
In this example, a symmetric key is generated for this credential and added to the service principal using the service principal name value of "MyApp/myApp.com".

### -------------------------- EXAMPLE 2 --------------------------
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate
          $cer.Import("C:\myapp.cer")
          $binCert = $cer.GetRawCertData()
          $credValue = [System.Convert]::ToBase64String($binCert);
          New-MsolServicePrincipalCredential -ServicePrincipalName "MyApp/myApp.com" -Type asymmetric -Value $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()

          New credential object added, including the KeyId for the added credential.
```

Description

-----------

This command adds a credential (or a key) object to an existing service principal.
In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using the service principal name value of "MyApp/myApp.com".

### -------------------------- EXAMPLE 3 --------------------------
```
New-MsolServicePrincipalCredential -AppPrincipalId  -Type asymmetric -Value $credValue

          New credential object added, including the KeyId for the added credential.
```

Description

-----------

This command shows how to register an on-premises Exchange Server so that communications between the Exchange Server and Microsoft Azure Active Directory services such as Office 365 can occur.
This example assumes that $credValue contains the base64 encoded public X509 certificate used to represent the on-premises Exchange server.
The well known Ids for Office 365 servers are:
            Exchange: 00000002-0000-0ff1-ce00-000000000000
            SharePoint: 00000003-0000-0ff1-ce00-000000000000
            Lync: 00000004-0000-0ff1-ce00-000000000000

## PARAMETERS

### -AppPrincipalId
The application ID associated with the service principal to add the credential to.

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
The effective end date of the credential usage.
The default end date value is one year from today. 
For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid until, otherwise an OAuth token will not be issued for this application.

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
The object ID of the service principal to add the credential to.

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
The unique name of the service principal to add the credential to.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL. 
AppName represents the name of the application and hostname represents the URI authority for the application.

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
The effective start date of the credential usage.
The default start date value is today. 
For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from, otherwise an OAuth token will not be issued for this application.

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

### -Type
The type of credential used.
The credential type can either be set to "asymmetric", "symmetric" or "password".
The default setting is "symmetric".

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
The usage of the credential key.
The credential key usage can either be set to "sign" or "verify" a token. 
The default setting is "verify". 
Sign is allowed ONLY for symmetric keys. 
Verify is allowed for all key types.
            A "verify" credential key is required by the Microsoft Azure Active Directory directory to verify that the request token was sent by your application (represented by this service principal).
Your application may optionally require that Microsoft Azure Active Directory services issue tokens to your application signed with your signing key rather than the asymmetric public key identifying Microsoft Azure Active Directory.
In this case, provide a "sign" credential key for your service principal.

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
The value of the credential.
If the credential type is set to "asymmetric", it represents the base 64 encoded certificate.
If the credential type is set to "symmetric" and Value is not set, a 256 bit AES key will be automatically created and valid for one year from creation.
If the credential type is set to "password", the Value parameter must be supplied and it should not be base 64 encoded.

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


