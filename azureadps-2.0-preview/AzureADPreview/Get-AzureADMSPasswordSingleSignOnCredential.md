---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSPasswordSingleSignOnCredential

## SYNOPSIS
Gets the password SSO credentials

## SYNTAX

```
Get-AzureADMSPasswordSingleSignOnCredential -ObjectId <String> -PasswordSSOObjectId <PasswordSSOObjectId>
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet enables users to read their Password Single-sign-on credentials for an application which they are part of.
Admin could read the group credentials as well.
Note that the password field will be hidden for security purpose.

## EXAMPLES

### Get password single-sign-on credentials
```
PS C:\> $get_creds_output = Get-AzureADMSPasswordSingleSignOnCredential -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -PasswordSSOObjectId bbbbbbbb-1111-2222-3333-cccccccccccc
```

This command gets the password sso credentials for the given ObjectId and PasswordSSOObjectId.

## PARAMETERS

### -ObjectId
The unique identifier of the object specific Azure Active Directory object

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PasswordSSOObjectId
User or group id

```yaml
Type: PasswordSSOObjectId
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.PasswordSSOCredentials
## NOTES
## RELATED LINKS
