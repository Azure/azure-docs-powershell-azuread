---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 20C36069-42AE-4B9C-A64B-ECAF5C3B6252
---

# Get-MsolDomain

## SYNOPSIS
Gets a domain in Azure Active Directory.

## SYNTAX

### ListDomains__0 (Default)
```
Get-MsolDomain [-Status <DomainStatus>] [-Authentication <DomainAuthenticationType>]
 [-Capability <DomainCapabilities>] [-TenantId <Guid>] [<CommonParameters>]
```

### GetDomain__0
```
Get-MsolDomain -DomainName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolDomain cmdlet gets company domains in Azure Active Directory.

## EXAMPLES

### Example 1: Get all domains for a company.

```
PS C:\> Get-Domain
```

This command retrieves all domains for the company, including verified and unverified domains.

### Example 2: Get a domain

```
PS C:\> Get-Domain -Name "contoso.com"
```

This command retrieves the contoso.com domain.

### Example 3: Get verified domains

```
PS C:\> Get-Domain -Status Verified
```

This command returns verified company domains.

## PARAMETERS

### -Authentication
Specifies an authentication type.
This cmdlet returns only domains that have this authentication type.

```yaml
Type: DomainAuthenticationType
Parameter Sets: ListDomains__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Capability
Specifies domain capability.
This cmdlet returns only domains that have the specified capability assigned.

```yaml
Type: DomainCapabilities
Parameter Sets: ListDomains__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName
Specifies the fully qualified domain name of the domain to return.

```yaml
Type: String
Parameter Sets: GetDomain__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Specifies domain status.
Valid values are: Verified, Unverified, and PendingDeletion.
This cmdlet returns only domains that have the specified status.

```yaml
Type: DomainStatus
Parameter Sets: ListDomains__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Domain
This cmdlet returns domain objects that include the following information:

* Authentication. The authentication type of the domain, which is managed or federated.
* Capabilities. The capabilities assigned to the domain.
These can be SharePoint, Email, or OfficeCommunicationsOnline.
A domain with SharePoint capability cannot be used for other capabilities.
* IsDefault. This is the default domain that is used for user creation.
There is only one default domain per company.
* IsInitial. Whether or not this is the initial domain created by Azure Active Directory (\[companyname\].onmicrosoft.com).
* Name. The full name of the domain.
* RootDomain. For subdomains, this represents the root domain.
Only root domains need to be verified, and all subdomains will be automatically verified.
* Status. The status of the domain, which is verified or unverified.

## NOTES

## RELATED LINKS
[Confirm-MsolDomain](./Confirm-MsolDomain.md)

[New-MsolDomain](./New-MsolDomain.md)

[Remove-MsolDomain](./Remove-MsolDomain.md)

[Set-MsolDomain](./Set-MsolDomain.md)
