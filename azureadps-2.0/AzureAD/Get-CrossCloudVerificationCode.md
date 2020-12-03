---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-CrossCloudVerificationCode

## SYNOPSIS
Gets the verification code used to validate the ownership of the domain in another connected cloud.
Important: Only applies to a verified domain.

## SYNTAX

```
Get-CrossCloudVerificationCode -Name <String> [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1: Get the cross cloud verification code
```
PS C:\>Get-CrossCloudVerificationCode -Name Contoso.com
```

This command will return a string that can be used to enable cross cloud federation scenarios.

## PARAMETERS

### -Name
Specifies the name of a domain.

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

### Microsoft.Online.Administration.GetCrossCloudVerificationCodeResponse
## NOTES
## RELATED LINKS
