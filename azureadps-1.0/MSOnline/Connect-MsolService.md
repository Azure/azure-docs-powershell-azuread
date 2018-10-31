---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: A5A10B0B-7C64-4778-8B42-EB073E2ADA92
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Connect-MsolService

## SYNOPSIS
Initiates a connection to Azure Active Directory.

## SYNTAX

### None__0 (Default)
```
Connect-MsolService [-AzureEnvironment <AzureEnvironment>] [<CommonParameters>]
```

### Credential
```
Connect-MsolService [-Credential <PSCredential>] [-AzureEnvironment <AzureEnvironment>] [<CommonParameters>]
```

### AccessToken
```
Connect-MsolService [-AdGraphAccessToken <String>] [-MsGraphAccessToken <String>]
 [-AzureEnvironment <AzureEnvironment>] [<CommonParameters>]
```

## DESCRIPTION
The **Connect-MsolService** cmdlet attempts to initiate a connection to Azure Active Directory.
You must specify a credential, as a **PSCredential** object, or specify the _CurrentCredentials_ parameter to use the credentials of the current user.

This cmdlet may return a warning or error if the version of the module is out of date.

## EXAMPLES

### Example 1: Initiate a connection
```
PS C:\> Connect-MsolService
```

This command attempts to initiate a connection with Azure Active Directory.
Since no credential is provided, the cmdlet prompts you to enter your username and password.

### Example 2: Initiate a connection by using a credential object
```
PS C:\> Connect-MsolService -Credential $Credential -AzureEnvironment AzureChinaCloud
```

This command attempts to initiate a connection to AzureChinaCloud with Azure Active Directory using the credential provided.
The credential must be of the type **PSCredential**.
To obtain a credential object, use the **Get-Credential** cmdlet.

## PARAMETERS

### -Credential
Specifies the credential to use to connect to Azure Active Directory.
To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.

```yaml
Type: PSCredential
Parameter Sets: Credential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdGraphAccessToken
Specifies the AD Graph access token to use to connect to Azure Active Directory.

```yaml
Type: String
Parameter Sets: AccessToken
Aliases: AccessToken

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MsGraphAccessToken
Specifies the MS Graph access token to use to connect to Azure Active Directory.

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

### -AzureEnvironment
Specifies the deployment type to use to connect to Azure Active Directory in different region.
Valid values are:

* AzureCloud
* AzureChinaCloud
* AzureGermanyCloud
* USGovernment

```yaml
Type: AzureEnvironment
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
