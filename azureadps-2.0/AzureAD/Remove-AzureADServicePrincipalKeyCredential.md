---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Remove-AzureADServicePrincipalKeyCredential

## SYNOPSIS
Removes a key credential from a service principal.

## SYNTAX

```
Remove-AzureADServicePrincipalKeyCredential -ObjectId <String> -KeyId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureADServicePrincipalKeyCredential cmdlet removes a key credential from a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1
```powershell
PS C:\> $SPObjectID = (Get-AzureADServicePrincipal -SearchString 'Azure Multi-Factor Auth Client').ObjectID
PS C:\> Get-AzureADServicePrincipalKeyCredential -ObjectId $SPObjectID
PS C:\> Remove-AzureADServicePrincipalKeyCredential -ObjectID $SPObjectID -KeyId <PASTE_KEYID_VALUE>
```

The first part of the examples stores the ObjectID of your service principal in the $SPObjectID variable. The second part gets all the Key Credentials for the service principal.
Copy the preferred **KeyID** associated with the certificate to be removed and paste it at the **<PASTE_KEYID_VALUE>** in the third part of the example.<br>
This removes the certificate (key credential) from the service principal configuration.

## PARAMETERS

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

### -KeyId
Specifies the ID of a key credential.

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

### -ObjectId
Specifies the ID of a service principal.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServicePrincipalKeyCredential]()

[New-AzureADServicePrincipalKeyCredential]()

