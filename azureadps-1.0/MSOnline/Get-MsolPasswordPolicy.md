---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 85A8F5D8-EDF3-4B49-A806-C95280EE370A
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolPasswordPolicy

## SYNOPSIS
Gets the current password policy for a tenant or a domain.

## SYNTAX

```
Get-MsolPasswordPolicy -DomainName <String> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolPasswordPolicy** cmdlet gets the values associated with the Password Expiry window or Password Expiry Notification window for a tenant or specified domain.
If you specify a domain name, it must be a verified domain for the company.

## EXAMPLES

### Example 1: Get the password policy for the tenant
```
PS C:\> Get-MsolPasswordPolicy
```

This command gets the password policy for the tenant.

### Example 2: Get the password policy for a domain
```
PS C:\> Get-MsolPasswordPolicy -DomainName contoso.com
```

This command gets the password policy for the domain contoso.com.

## PARAMETERS

### -DomainName
Specifies the fully qualified domain name of the domain to be retrieved.

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

###  
This cmdlet returns the following values:

* ValidityPeriod. Specifies the length of time that a password is valid before it must be changed.
A null value indicates the default value of 90 days will be used.

* NotificationDays. Specifies the number of days before a user receives notification that their password will expire.
A null value indicates the default of 14 days will be used.

## NOTES

## RELATED LINKS
[Set-MsolPasswordPolicy](./Set-MsolPasswordPolicy.md)
