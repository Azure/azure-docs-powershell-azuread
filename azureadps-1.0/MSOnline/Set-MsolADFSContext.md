---
external help file: Microsoft.Online.Identity.Federation.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0BCF8D45-6F60-42BD-81A0-EE3F3709AF7E
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolADFSContext

## SYNOPSIS
Sets the context and credentials to connect to Microsoft Online and to the Active Directory Federation Services 2.0 server.

## SYNTAX

```
Set-MsolADFSContext [-ADFSUserCredentials <PSCredential>] -Computer <String> [-LogFile <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolADFSContext** cmdlet sets the credentials to connect to Microsoft Online and to the Active Directory Federation Services 2.0 (AD FS 2.0) server.
This cmdlet must be run before running other single sign-on cmdlets.
Single sign-on is also known as identity federation.

If you do not specify parameters for this cmdlet, you are prompted for credentials to connect to the different systems.

If the AD FS 2.0 server is used remotely, you must specify the computer name of the primary AD FS 2.0 server.

The specified logfile is shared by all single sign-on cmdlets for the session.
A default logfile is created if one is not specified.

## PARAMETERS

### -ADFSUserCredentials
Specifies the credential object used to establish the administrative session on the Active Directory Federation Services 2.0 server.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Computer
Specifies computer name of the primary AD FS 2.0 server.
Specify this parameter if the AD FS 2.0 server is used remotely.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogFile
Specifies the log file used to log all single sign-on cmdlet operations for the Windows PowerShell session.
If not specified, the Windows PowerShell module creates a log file in %USERPROFILE%\Documents\MicrosoftOnline.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
