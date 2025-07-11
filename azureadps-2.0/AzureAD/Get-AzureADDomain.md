---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADDomain

## SYNOPSIS
Gets a domain.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDomain [<CommonParameters>]
```

### GetById
```
Get-AzureADDomain -Name <String> [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADDomain cmdlet gets a domain in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a list of Domains that have been created.
```powershell
PS C:\>Get-AzureADDomain

Name        AvailabilityStatus AuthenticationType
----        ------------------ ------------------
Contoso.com                    Managed
Fabrikam.com                   Managed
Adatum.com                     Managed
```

This command retrieves a list of domains.

### Example 2: Get a specific Domain.
```powershell
PS C:\>Get-AzureADDomain -Name Contoso.com

Name        AvailabilityStatus AuthenticationType
----        ------------------ ------------------
Contoso.com                    Managed
```

This command retrieves a domain with the specified name.

## PARAMETERS

### -Name
Specifies the name of a domain.

```yaml
Type: String
Parameter Sets: GetById
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

See the [migration guide for Get-AzureADDomain](./migrate/Get-AzureADDomain.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Confirm-AzureADDomain](Confirm-AzureADDomain.md)

[New-AzureADDomain](New-AzureADDomain.md)

[Remove-AzureADDomain](Remove-AzureADDomain.md)

[Set-AzureADDomain](Set-AzureADDomain.md)

