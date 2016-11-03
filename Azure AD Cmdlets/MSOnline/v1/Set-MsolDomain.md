---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 750DB368-6EC8-45AC-B3E8-A4D53E6284D7
---

# Set-MsolDomain

## SYNOPSIS
Updates the settings of a domain.

## SYNTAX

```
Set-MsolDomain [-Name <String>] [-IsDefault] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolDomain cmdlet is used to update settings for a domain.
Using this cmdlet, the default domain can be changed, or the capabilities (Email, Sharepoint, OfficeCommunicationsOnline) can be changed.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
set-msoldomain -name example.com -IsDefault
```

Description

-----------

Will set example.com as the default domain for this company.

## PARAMETERS

### -IsDefault
A switch parameter to make this domain the default domain.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
The name of the domain to update.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


