---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: B44214C0-6CFA-4169-8E09-8C4065DFAB2E
---

# Remove-MsolDomain

## SYNOPSIS
Removes a domain from Microsoft Azure Active Directory.

## SYNTAX

```
Remove-MsolDomain -DomainName <String> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolDomain cmdlet is used to delete a domain from Microsoft Azure Active Directory.
The domain being deleted must be empty; that is, there cannot be any users or groups with email addresses in this domain.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolDomain -DomainName contoso.com -force

          None
```

Description

-----------

This command attempts to remove the domain contoso.com. 
This operation will fail if there are any users or groups that reference the domain.

## PARAMETERS

### -DomainName
The fully qualified domain name (FQDN) to remove.

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
Used to bypass onscreen confirmation.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


