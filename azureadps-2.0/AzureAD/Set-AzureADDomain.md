---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADDomain

## SYNOPSIS
Updates a domain.

## SYNTAX

```
Set-AzureADDomain -Name <String> [-IsDefault <Boolean>] [-IsDefaultForCloudRedirections <Boolean>]
 [-SupportedServices <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADDomain cmdlet updates a domain in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Set the domain as the default domain for new user account creation
```
PS C:\>Set-AzureADDomain -Name Contoso.com -IsDefault $true
```

This command updates the default domain (One per company) used for new account creation.

### Example 2: Set the list of domain capabilities
```
PS C:\>Set-AzureADDomain -Name Contoso.com -SupportedServices @("Email", "OfficeCommunicationsOnline")
```

This command updates the supported services for this domain.

### Example 3: Set the default domain for cloud redirections
```
PS C:\>Set-AzureADDomain -Name Contoso.com -IsDefaultForCloudRedirections $true
```

This command updates the default domain used for cloud redirections.

## PARAMETERS

### -IsDefault
Indicates whether or not this is the default domain that is used for user creation.
There is only one default domain per company.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDefaultForCloudRedirections
Indicates whether or not this is the default domain used for cloud redirections.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The fully qualified name of the domain.

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

### -SupportedServices
The capabilities assigned to the domain.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Confirm-AzureADDomain]()

[Get-AzureADDomain]()

[New-AzureADDomain]()

[Remove-AzureADDomain]()

