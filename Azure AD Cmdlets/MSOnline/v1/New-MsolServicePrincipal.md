---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 90C7E9B8-165A-4628-8399-F71F371FBB42
---

# New-MsolServicePrincipal

## SYNOPSIS
Add a new service principal to the Microsoft Azure Active Directory.

## SYNTAX

```
New-MsolServicePrincipal [-ServicePrincipalNames <String[]>] [-AppPrincipalId <Guid>] -DisplayName <String>
 [-AccountEnabled <Boolean>] [-Addresses <RedirectUri[]>] [-Type <ServicePrincipalCredentialType>]
 [-Value <String>] [-StartDate <DateTime>] [-EndDate <DateTime>] [-Usage <ServicePrincipalCredentialUsage>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The New-MsolServicePrincipal cmdlet creates a service principal that can be used to represent a Line Of Business (LOB) application or an on-premises server such as Microsoft Exchange, SharePoint or Lync in Microsoft Azure Active Directory as "service principal" objects.
Adding a new application as a service principal allows that application to authenticate to other services such as Microsoft Office 365.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
New-MsolServicePrincipal -ServicePrincipalNames @("MyApp/myApp.com") -DisplayName "My Application"

          New service principal object created.
```

Description

-----------

This command creates a new service principal.
In this example, the service principal will be created with the service principal name "MyApp/myApp.com", the display name "My Application", and will use an auto-generated 256 bit symmetric key to verify the application.
This key will be valid for a year from today.

### -------------------------- EXAMPLE 2 --------------------------
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate
          $cer.Import("C:\temp\myapp.cer")
          $binCert = $cer.GetRawCertData()
          $credValue = [System.Convert]::ToBase64String($binCert);
          New-MsolServicePrincipal -ServicePrincipalNames @("MyApp/myApp.com") -DisplayName "My Application" -Type asymmetric -Value $credValue

          New service principal object created.
```

Description

-----------

This command creates a new service principal.
In this example, the service principal will be created with the service principal name "MyApp/myApp.com", the display name "My Application", and will use the supplied X509 certificate "myapp.cer" that is configured with a base 64 encoded asymmetric key.

## PARAMETERS

### -AccountEnabled
Specifies if the account needs to be enabled.
This will be set to true if not specified.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: True
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Addresses
List of addresses used by the application. 
The list should be constructed by using the New-MsolServicePrincipalAddress help cmdlet.

```yaml
Type: RedirectUri[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AppPrincipalId
The unique application identifier for a service principal in a tenant.
Once created this property cannot be changed.
If an AppPrincipalId is not specified, one will be generated.

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

### -DisplayName
The friendly name of the service principal

```yaml
Type: String
Parameter Sets: (All)
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

### -ServicePrincipalNames
A list of service principal names (SPNs) associated with the service principal.
            An SPN must be unique per company tenant and is used by an application to uniquely identify itself. 
By default the service principal AppID is always added as an SPN.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL. 
AppName represents the name of the application and hostname represents the URI authority for the application. 
When the service principal represents a WS-Federation relying party, an SPN can be set to a URL that would be treated as the WS-Federation wtrealm parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: AppId of the service principal
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDate
The effective start date of the credential usage.
The default start date value is today.

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
If "asymmetric", the Value parameter must be set to the public portion of a base 64 encoded X509 certificate. 
If "symmetric", then a 256 bit AES symmetric key will be generated if Value is not set. 
If "password", the Value parameter must be supplied and it should not be base 64 encoded. 
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
            A "verify" credential key is required by Microsoft Azure Active Directory to verify that the request token was sent by your application (represented by this service principal).
Your application may optionally require that Microsoft Azure Active Directory issue tokens to your application signed with your signing key rather than the asymmetric public key identifying Microsoft Azure Active Directory.
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

### Microsoft.Online.Administration.ServicePrincipalExtended
Retrieves the service principal that it added with the following information:

            ObjectId - The unique identifier of the service principal.
            AppPrincipalId - The application identifier of the service principal.
            DisplayName - The friendly name of the service principal.
            ServicePrincipalName - The list of service principal names (SPNs) associated with the service principal.
            TrustedForDelegation - The value indicating if the service principal is allowed for delegation.
            AccountEnabled - The value indicating if the account is enabled.

            It also retrieves the list of credentials that were added.
Each credential object will contain the following information:

            Type - The type of service principal credential (Asymmetric/Symmetric/Other).
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


