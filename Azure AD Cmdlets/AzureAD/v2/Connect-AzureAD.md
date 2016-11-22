---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Connect-AzureAD

## SYNOPSIS
Connect with an authenticated account to use Azure Active Directory cmdlet requests.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Connect-AzureAD [-AzureEnvironmentName <AzureEnvironment+EnvironmentName>] [-TenantId <String>]
 [-Credential <PSCredential>] [-LogLevel <LogLevel>] [-WhatIf] [-Confirm]
```

### UNNAMED_PARAMETER_SET_2
```
Connect-AzureAD [-AzureEnvironmentName <AzureEnvironment+EnvironmentName>] [-TenantId <String>]
 [-LogLevel <LogLevel>] [-WhatIf] [-Confirm] -CertificateThumbprint <String> -ApplicationId <String>
```

### UNNAMED_PARAMETER_SET_3
```
Connect-AzureAD [-AzureEnvironmentName <AzureEnvironment+EnvironmentName>] [-TenantId <String>]
 [-LogLevel <LogLevel>] [-WhatIf] [-Confirm] -AadAccessToken <String> [-MsAccessToken <String>]
 -AccountId <String>
```

## DESCRIPTION
The Connect-AzureAD cmdlet connects an authenticated account to use for Azure Active Directory cmdlet requests.

## EXAMPLES

### Connect a powershell session to an azure AD tenant
```
Connect-AzureAD
```

This will connect your current PowerShell session to an AzureAD tenant.
The command will prompt for a username and password for the tenant you want to connect to.
The -Confirm parameter will bring up the prompt for confirmation.


If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.

### Get credentials from the user, then connect the powershell session tot the tenant for those credentials
```
$Credential = Get-Credential
; Connect-AzureAD -Credential $Credential
```

The first command gets the user credentials, and then stores them in the $Credential variable.


The second command connect your current PowerShell session with the credentials in $Credential.


This account authenticates with AzureAD using organizational ID credentials.
You cannot use multi-factor authentication or Microsoft account credentials to run AzureAD cmdlets with this account.

### Connect your PowerShell session to a tenant using service principal credentials
```
Connect-AzureAD -TenantId "xxxx-xxxx-xxxx-xxxx" -ApplicationId "xxxx-xxxx-xxxx-xxxx" -CertificateThumbprint "xxxx-xxxx-xxxx-xxxx"
```

The command authenticate you to AzureAD as a service principal.

### Connect your PowerShell session to a tenant in a specific environment
```
Connect-AzureAD -AzureEnvironmentName AzureADChinaCloud
```

Permissable values are AzureCloud, AzurePPE, AzureGermanyCloud, AzureChinaCloud and USGovernment

## PARAMETERS

### -AzureEnvironmentName
Specifies the Azure environment.
Valid values are: AzureCloud, AzureChinaCloud, AzureUSGovernment and AzureGermanyCloud.
The default is AzureCloud.

```yaml
Type: AzureEnvironment+EnvironmentName
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Specifies a tenant.
If you do not specify this parameter, the account is authenticated to the home tenant of the user.
You must specify the TenantID parameter to authenticate as a service principal or using Microsoft account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifies a PSCredential object.
For more information about the PSCredential object, type Get-Help Get-Credential.
The PSCredential object provides the user ID and password for organizational ID credentials.
Note that you cannot connect to a tenant using the credential parameter if Multi Factor Authentication is enabled for the account

```yaml
Type: PSCredential
Parameter Sets: UNNAMED_PARAMETER_SET_1
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
The log file is in %localappdata%\Microsoft\AzureAD\Powershell

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

### -WhatIf
@{Text=}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Secret for service principal credentials.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
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
Parameter Sets: UNNAMED_PARAMETER_SET_2
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
Parameter Sets: UNNAMED_PARAMETER_SET_3
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
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
The UPN of the user when authenticating with a user access token.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

