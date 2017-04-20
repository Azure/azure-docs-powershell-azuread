---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: 9E9EE157-A923-4643-8DA5-E1A27EFB61E0
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalKeyCredential

## SYNOPSIS
Get key credentials for a service principal.

## SYNTAX

```
Get-AzureADServicePrincipalKeyCredential -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADServicePrincipalKeyCredential** cmdlet gets the key credentials for a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve the key credential of a service principal
```
PS C:\> $ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> Get-AzureADServicePrincipalKeyCredential -ObjectId $ServicePrincipalId
```

The first command gets the ID of a service principal by using the [Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md) cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets the key credential for the service principal identified by $ServicePrincipalId.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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

### -ObjectId
Specifies the ID of the application for which to get the password credential.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)

[New-AzureADServicePrincipalKeyCredential](./New-AzureADServicePrincipalKeyCredential.md)

[Remove-AzureADServicePrincipalKeyCredential](./Remove-AzureADServicePrincipalKeyCredential.md)
