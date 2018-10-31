---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D1BC57E1-276A-4DDE-9923-227BCAA59985
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolPasswordPolicy

## SYNOPSIS
Updates the password policy of a specified domain or tenant.

## SYNTAX

```
Set-MsolPasswordPolicy -DomainName <String> [-ValidityPeriod <UInt32>] [-NotificationDays <UInt32>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolPasswordPolicy** cmdlet updates the password policy of a specified domain or tenant.
Two settings are required, the first is to indicate the length of time that a password remains valid before it must be changed and the second is to indicate the number of days before the password expiration date that will trigger when users will receive their first notification that their password will soon expire.

## EXAMPLES

### Example 1: Update validity period and notification for the current domain
```
PS C:\> Set-MsolPasswordPolicy -ValidityPeriod 60 -NotificationDays 14
```

This command updates the tenant so that all users passwords expire after 60 days.
The users receive notification 14 days prior to that expiry.

### Example 2: Update validity period and notification for a domain
```
PS C:\> Set-MsolPasswordPolicy -ValidityPeriod 60 -NotificationDays 14 -DomainName "contoso.com"
```

This command updates the policy on the domain contoso.com so that users passwords expire after 60 days.
The users receive notification 14 days prior to that expiry.

## PARAMETERS

### -DomainName
Specifies the fully qualified domain name to which to apply policies.

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

### -NotificationDays
Specifies the number of days before the password expiration date that triggers when users receive their first notification that their password will soon expire.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidityPeriod
Specifies the length of time that a password is valid before it must be changed.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
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

## NOTES

## RELATED LINKS
[Get-MsolPasswordPolicy](./Get-MsolPasswordPolicy.md)
