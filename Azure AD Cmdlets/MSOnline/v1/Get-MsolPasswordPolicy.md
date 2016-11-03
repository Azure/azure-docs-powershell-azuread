---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 85A8F5D8-EDF3-4B49-A806-C95280EE370A
---

# Get-MsolPasswordPolicy

## SYNOPSIS
Retrieves the current password policy for the tenant or the specified domain.

## SYNTAX

```
Get-MsolPasswordPolicy -DomainName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolPasswordPolicy cmdlet can be used to retrieve the values associated with the Password Expiry window or Password Expiry Notification window for a tenant or specified domain. 
When a domain name is specified, it must be a verified domain for the company.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolPasswordPolicy

          Returns the password policy.
```

Description

-----------

Returns the password policy for the tenant.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MsolPasswordPolicy -DomainName contoso.com

          Returns the password policy.
```

Description

-----------

Returns the password policy for the domain contoso.com.

## PARAMETERS

### -DomainName
The fully qualified name of the domain to be retrieved.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId


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

###  
The following values will be returned either for the specified domain or the tenant if no domain was specified.

            ValidityPeriod : Specifies the length of time that a password is valid before it must be changed.
A null value indicates the default value of 90 days will be used.

            NotificationDays : Specifies the number of days before a user receives notification that their password will expire.
A null value indicates the default of 14 days will be used.

## NOTES

## RELATED LINKS


