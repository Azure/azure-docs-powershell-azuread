---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: B44214C0-6CFA-4169-8E09-8C4065DFAB2E
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolDomain

## SYNOPSIS
Removes a domain from Azure Active Directory.

## SYNTAX

```
Remove-MsolDomain -DomainName <String> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolDomain** cmdlet is used to delete a domain from Azure Active Directory.
The domain being deleted must be empty.
There cannot be any users or groups with email addresses in this domain.

## EXAMPLES

### Example 1: Remove a domain

```
PS C:\> Remove-MsolDomain -DomainName "contoso.com" -Force
```

This command attempts to remove the domain contoso.com without prompting you for confirmation.
This operation fails if there are any users or groups that reference the domain.

## PARAMETERS

### -DomainName
Specifies the fully qualified domain name (FQDN) of the domain to remove.

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

### -Force
Indicates that this cmdlet does not prompt you for confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

## NOTES

## RELATED LINKS
[Confirm-MsolDomain](./Confirm-MsolDomain.md)

[Get-MsolDomain](./Get-MsolDomain.md)

[New-MsolDomain](./New-MsolDomain.md)

[Set-MsolDomain](./Set-MsolDomain.md)
