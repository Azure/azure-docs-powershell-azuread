---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDomainServiceConfigurationRecord

## SYNOPSIS
Gets the domain's service configuration records from the serviceConfigurationRecords navigation property.

## SYNTAX

```
Get-AzureADDomainServiceConfigurationRecord -Name <String> [<CommonParameters>]
```

## DESCRIPTION
Gets the domain's service configuration records from the serviceConfigurationRecords navigation property. 
After you have successfully verified the ownership of a domain and you have indicated what services you plan to use with the domain, you can request Azure AD to return you a set of DNS records which you need to add to the zone file of the domain so that the services can work properly with your domain.

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADDomainServiceConfigurationRecord -name drumkit.onmicrosoft.com

DnsRecordId                          Label                                          SupportedService           Ttl
-----------                          -----                                          ----------------           ---
2b672ab0-0bee-476f-b334-be436f2449bd drumkit.onmicrosoft.com                        Email                      3600
62bea837-a0d7-4466-b6d9-ff6bd1db8671 drumkit.onmicrosoft.com                        Email                      3600
eea5ce9e-8deb-4ab7-a114-13ed6215774f autodiscover.drumkit.onmicrosoft.com           Email                      3600
2f9deed0-42e3-4f6d-ae82-495a7fde4da5 _sip._tls.drumkit.onmicrosoft.com              OfficeCommunicationsOnline 3600
e9046b54-7d0d-422f-9e50-c731b2a8cbd5 sip.drumkit.onmicrosoft.com                    OfficeCommunicationsOnline 3600
a2a182ac-0b69-44c3-96c6-5d6bbbe9ee99 lyncdiscover.drumkit.onmicrosoft.com           OfficeCommunicationsOnline 3600
b457cd8d-e1bb-4ea9-ae65-cb31c551e27a _sipfederationtls._tcp.drumkit.onmicrosoft.com OfficeCommunicationsOnline 3600
```

This example shows how to retrieve the Domain service configuration records for a domain with the given name

## PARAMETERS

### -Name
The name of the domain for which the domain service configuration records are to be retrieved

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

