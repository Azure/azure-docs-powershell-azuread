---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D0D10A71-D935-4D24-B671-F8E0A5D8979D
---

# New-MsolAdministrativeUnit

## SYNOPSIS
Adds a new administrative unit to Azure Active Directory.

## SYNTAX

```
New-MsolAdministrativeUnit [-DisplayName <String>] [-Description <String>] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-MsolAdministrativeUnit cmdlet adds a new administrative unit to Azure Active Directory.

## EXAMPLES

### --------------------------  Example 1  --------------------------
@{paragraph=PS C:\\\>}



```
New-MsolAdministrativeUnit -DisplayName "West Coast" -Description "West Coast region"
```

Description

-----------

This command creates a new administrative unit called "West Coast" that has a description "West Coast region".

## PARAMETERS

### -DisplayName
The display name of the administrative unit.

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

### -Description
The description of the administrative unit.

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

### Microsoft.Online.Administration.AdministrativeUnit
Will return the new administrative unit that was created.

## NOTES

## RELATED LINKS


