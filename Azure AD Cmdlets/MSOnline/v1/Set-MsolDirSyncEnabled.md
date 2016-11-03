---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 2874711E-96F5-43E8-8D90-332C65A85FB5
---

# Set-MsolDirSyncEnabled

## SYNOPSIS
Used to de-/activate Directory Sync for this tenant.

## SYNTAX

```
Set-MsolDirSyncEnabled -EnableDirSync <Boolean> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolDirSyncEnabled cmdlet is used to turn directory synchronization on or off for a company.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Set-MsolDirSyncEnabled -EnableDirsync $true

          None
```

Description

-----------

This command turns on directory synchronization for a company.

## PARAMETERS

### -EnableDirSync
When true, directory synchronization will be turned on for your company.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Force


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


