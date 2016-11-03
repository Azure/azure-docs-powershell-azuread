---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 013C6697-E78E-4882-840B-CC0595C452DA
---

# New-MsolDomain

## SYNOPSIS
Add a new domain to Microsoft Azure Active Directory.

## SYNTAX

```
New-MsolDomain [-Name <String>] [-Authentication <DomainAuthenticationType>]
 [-VerificationMethod <DomainVerificationMethod>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The New-MsolDomain cmdlet is used to create a new domain object.
This cmdlet can be used to create a domain with managed or federated identities, although the New-MsolFederatedDomain cmdlet should be used for federated domains in order to ensure proper setup.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
New-MsolDomain -Name contoso.com

          Returns a domain object.
```

Description

-----------

This command creates a new domain with the name contoso.com. 
The domain must be verified before it can be used.

## PARAMETERS

### -Authentication
The authentication type (managed or federated) of the domain. 
All users created in this domain will have this authentication type.

```yaml
Type: DomainAuthenticationType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
The fully qualified domain name of the domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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

### -VerificationMethod


```yaml
Type: DomainVerificationMethod
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
This cmdlet returns the details about the new domain.

## NOTES

## RELATED LINKS


