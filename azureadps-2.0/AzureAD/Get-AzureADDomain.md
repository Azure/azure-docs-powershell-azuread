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

### Example 1
```powershell
PS C:\>Get-AzureADDomain

Name        AvailabilityStatus AuthenticationType
----        ------------------ ------------------
Contoso.com                    Managed
Fabrikam.com                   Managed
Adatum.com                     Managed
```

This command retrieves a list of domains.

### Example 2: Get a specific Domain
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

## RELATED LINKS

[Confirm-AzureADDomain]()

[New-AzureADDomain]()

[Remove-AzureADDomain]()

[Set-AzureADDomain]()

