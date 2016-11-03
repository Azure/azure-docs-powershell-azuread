---
external help file: Microsoft.Online.Identity.Federation.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 0BCF8D45-6F60-42BD-81A0-EE3F3709AF7E
---

# Set-MsolADFSContext

## SYNOPSIS
Sets the context and credentials to connect to Microsoft Online and to the Active Directory Federation Services 2.0 server.
This cmdlet also records the logging file location.

## SYNTAX

```
Set-MsolADFSContext [-ADFSUserCredentials <PSCredential>] -Computer <String> [-LogFile <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolADFSContext cmdlet sets the credentials to connect to Microsoft Online and to the Active Directory Federation Services 2.0 (AD FS 2.0) server.
This cmdlet must be run before making other single sign-on (also known as identity federation) cmdlet calls.
If this cmdlet is called without parameters, the user will be prompted for credentials to connect to the different systems.
When the AD FS 2.0 server is used remotely, the user must specify the computer name of the primary AD FS 2.0 server.
Note that the specified logfile is shared by all single sign-on cmdlets for the session.
A default logfile is created if one is not specified.

## PARAMETERS

### -ADFSUserCredentials
The credential object used to establish the administrative session on the Active Directory Federation Services 2.0 server.

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
The computer name of the primary AD FS 2.0 server.
Specify this when the AD FS 2.0 server is used remotely.

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
The log file used to log all single sign-on cmdlet operations for the Windows PowerShell session.
If not specified, the Windows PowerShell module will auto-create a log file in %USERPROFILE%\Documents\MicrosoftOnline

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


