---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 4E3EE703-F105-449D-B74E-8C4B70E63A90
---

# Get-MsolPartnerContract

## SYNOPSIS
Retrieves a list of contracts for a partner.

## SYNTAX

### ListPartnerContracts__0 (Default)
```
Get-MsolPartnerContract [-DomainName <String>] [-SearchKey <PartnerContractSearchKey>] [-MaxResults <Int32>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolPartnerContract [-DomainName <String>] [-SearchKey <PartnerContractSearchKey>] [-All]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolPartnerContract cmdlet should only be used by partners, as it is used to retrieve a list of contracts for a partner.
The input to this cmdlet should be a domain to look up, which must be verified for the tenant.
If the company exists and the partner has access to this company, then the corresponding contract will be returned.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolPartnerContract -DomainName contoso.com

          Returns a contract object.
```

Description

-----------

This command returns the contract for the tenant owning the domain consoso.com. 
The caller must have privileges to act on behalf of contoso.com.

## PARAMETERS

### -DomainName
The domain to search for.
This must be the full name of a verified domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
The tenant of the partner to retrieve contracts for.
If this is not provided, then the value will default to the tenant of the current user.
If this parameter is provided, the tenant ID must correspond to a partner company.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -All


```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults


```yaml
Type: Int32
Parameter Sets: ListPartnerContracts__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchKey


```yaml
Type: PartnerContractSearchKey
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.PartnerContract

## NOTES

## RELATED LINKS


