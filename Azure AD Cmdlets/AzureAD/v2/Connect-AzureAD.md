---
external help file: Microsoft.Open.Azure.AD.CommonLibrary.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: A5EF9C25-E0D9-432F-A528-81534A01F444
---

# Connect-AzureAD

## SYNOPSIS
Connect with an authenticated account to use Azure Active Directory cmdlet requests.

## SYNTAX

### User (Default)
```
Connect-AzureAD [-AzureEnvironmentName <EnvironmentName>] [-TenantId <String>] [-Credential <PSCredential>]
 [-LogLevel <LogLevel>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ServicePrincipalCertificate
```
Connect-AzureAD [-AzureEnvironmentName <EnvironmentName>] -TenantId <String> -CertificateThumbprint <String>
 -ApplicationId <String> [-LogLevel <LogLevel>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessToken
```
Connect-AzureAD [-AzureEnvironmentName <EnvironmentName>] [-TenantId <String>] -AadAccessToken <String>
 [-MsAccessToken <String>] -AccountId <String> [-LogLevel <LogLevel>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The Connect-AzureAD cmdlet connects an authenticated  account to use for Azure Active Directory cmdlet requests.

You can use this authenticated account only with Azure Active Directory cmdlets.

## EXAMPLES

### --------------------------  Example 1  --------------------------
```
PS C:\>Connect-AzureAD -Confirm
```

This will connect your current PowerShell session to an AzureAD tenant.
The command will prompt for a username and password for the tenant you want to connect to.
The -Confirm parameter will bring up the prompt for confirmation. 

If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.

### --------------------------  Example 2  --------------------------
```
PS C:\>$Credential = Get-Credential
PS C:\> Connect-AzureAD -Credential $Credential
```

The first command gets the user credentials, and then stores them in the $Credential variable.

The second command connect your current PowerShell session with the credentials in $Credential.

This account authenticates with AzureAD using organizational ID credentials.
You cannot use multi-factor authentication or Microsoft account credentials to run AzureAD cmdlets with this account.

### --------------------------  Example 3  --------------------------
```
PS C:\> Connect-AzureAD -TenantId "xxxx-xxxx-xxxx-xxxx" -ApplicationId "xxxx-xxxx-xxxx-xxxx" -CertificateThumbprint "xxxx-xxxx-xxxx-xxxx"
```

The command authenticate you to AzureAD as a service principal.

## PARAMETERS

### -AzureEnvironmentName
Specifies the Azure environment.
Valid values are: AzureCloud, AzureChinaCloud, AzureUSGovernment and AzureGermanyCloud.
The default is AzureCloud.

```yaml
Type: EnvironmentName
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Specifies a tenant.
If you do not specify this parameter, the account is authenticated for all available tenants.

You must specify the Tenant parameter to authenticate as a service principal or using Microsoft account.

```yaml
Type: String
Parameter Sets: User, AccessToken
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificate
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifies a PSCredential object.
For more information about the PSCredential object, type Get-Help Get-Credential.

The PSCredential object provides the user ID and password for organizational ID credentials.

```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogLevel
Specifies the log level.
Valid values are Info, Error, Warning, None.
Default level is Info.

```yaml
Type: LogLevel
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Secret for service principal credentials.

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Application ID of the service principal.

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AadAccessToken
Specifies a AAD Graph access token.

```yaml
Type: String
Parameter Sets: AccessToken
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MsAccessToken
Specifies a MS Graph access token.

```yaml
Type: String
Parameter Sets: AccessToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
You must specify UPN of the user when authenticate with user access token.

```yaml
Type: String
Parameter Sets: AccessToken
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


