---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 20C36069-42AE-4B9C-A64B-ECAF5C3B6252
---

# Get-MsolDomain

## SYNOPSIS
Retrieves a domain Microsoft Azure Active Directory.

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
The Get-MsolDomain cmdlet is used to retrieve company domains.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\> Get-Domain

          Returns a list of company domains.
```

Description

-----------

This command retrieves all domains for the company (verified or unverified).

### -------------------------- EXAMPLE 2 --------------------------
```
PS C:\> Get-Domain -Name contoso.com

          Returns a domain name.
```

Description

-----------

This command retrieves the contoso.com domain.

### -------------------------- EXAMPLE 3 --------------------------
```
PS C:\> Get-Domain -Status Verified

          Returns a list of verified company domains.
```

Description

-----------

This command returns a list of verified company domains .

## PARAMETERS

### -Authentication
The filter for the specified authentication type.
If provided, only domains with the authentication type will be returned.

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
The filter for domains that have the specified capability assigned.

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
The fully qualified domain name to retrieve.

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
The filter to return only domains with the specified status.
Valid values are Verified, Unverified, and PendingDeletion.

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
Each domain returned will include the following information:

            Authentication: The authentication type of the domain (managed or federated).

            Capabilities: The capabilities assigned to the domain.
These can be SharePoint, email, or OfficeCommunicationsOnline.
A domain with SharePoint capability cannot be used for other capabilities.

            IsDefault: This is the default domain that is used for user creation.
There is only one default domain per company.

            IsInitial: Whether or not this is the initial domain created by Microsoft Azure Active Directory (\[companyname\].onmicrosoft.com).

            Name: The full name of the domain.

            RootDomain: For subdomains, this represents the root domain.
Only root domains need to be verified, and all subdomains will be automatically verified.

            Status: The status of the domain (verified or unverified).

## NOTES

## RELATED LINKS
