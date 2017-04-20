---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDomainVerificationDnsRecord

## SYNOPSIS
Retrieve the domain verification DNS record for a domain

## SYNTAX

```
Get-AzureADDomainVerificationDnsRecord -Name <String> [<CommonParameters>]
```

## DESCRIPTION
Gets the domain's verification records from the verificationDnsRecords navigation property. 
You can ¢â‚¬â"¢t use the domain with your Azure AD tenant until you have successfully verified that you own the domain. To verify the ownership of the domain, you need to first retrieve a set of domain verification records which you need to add to the zone file of the domain.

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADDomainVerificationDnsRecord -Name drumkit.onmicrosoft.com

DnsRecordId                          Label                   SupportedService Ttl
-----------                          -----                   ---------------- ---
aceff52c-06a5-447f-ac5f-256ad243cc5c drumkit.onmicrosoft.com Email            3600
5fbde38c-0865-497f-82b1-126f596bcee9 drumkit.onmicrosoft.com Email            3600
```

This example shows how to retrieve the domain verification DNS records for the given domain name

## PARAMETERS

### -Name
The domain name for which the domain verification DNS records are to be retrieved

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

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

