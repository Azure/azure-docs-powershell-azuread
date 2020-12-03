---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Confirm-AzureADDomain

## SYNOPSIS
Validate the ownership of a domain.

## SYNTAX

```
Confirm-AzureADDomain -Name <String> [-CrossCloudVerificationCode <CrossCloudVerificationCodeBody>]
 [<CommonParameters>]
```

## DESCRIPTION
The Confirm-AzureADDomain cmdlet validates the ownership of an Azure Active Directory domain.

## EXAMPLES

### Example 1: Confirm the domain
```
PS C:\>Confirm-AzureADDomain -Name Contoso.com
```

This command will confirm your domain; changing the status to "Verified".

### Example 2: Confirm the domain with a cross cloud verification code
```
PS C:\>Confirm-AzureADDomain -Name Contoso.com -CrossCloudVerificationCode ms84324896
```

This command will confirm your domain for dual federation scenarios.

## PARAMETERS

### -Name
Specifies the name of the domain.

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

### -CrossCloudVerificationCode
The cross-cloud domain verification code.

```yaml
Type: CrossCloudVerificationCodeBody
Parameter Sets: (All)
Aliases:

Required: False
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

[Get-AzureADDomain]()

[New-AzureADDomain]()

[Remove-AzureADDomain]()

[Set-AzureADDomain]()

