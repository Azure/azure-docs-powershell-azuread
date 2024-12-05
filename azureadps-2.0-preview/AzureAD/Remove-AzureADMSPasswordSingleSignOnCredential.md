---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSPasswordSingleSignOnCredential

## SYNOPSIS
Removes the password SSO credentials

## SYNTAX

```
Remove-AzureADMSPasswordSingleSignOnCredential -ObjectId <String> -PasswordSSOObjectId <PasswordSSOObjectId>
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet enables users to remove their Password Single-sign-on credentials for an application which they are part of.
Admin could remove the group credentials as well.

## EXAMPLES

### Remove password single-sign-on credentials
```
PS C:\> Remove-AzureADMSPasswordSingleSignOnCredential -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb -PasswordSSOObjectId bbbbbbbb-1111-2222-3333-cccccccccccc
```

This command removes the password sso credentials for the given ObjectId and PasswordSSOObjectId.

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

## NOTES
## RELATED LINKS
