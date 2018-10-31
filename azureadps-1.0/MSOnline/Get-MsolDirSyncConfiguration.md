---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 174960FD-00BB-461F-B8C9-DDA519E24F00
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolDirSyncConfiguration

## SYNOPSIS
Gets the directory synchronization settings.

## SYNTAX

```
Get-MsolDirSyncConfiguration [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolDirSyncConfiguration** cmdlet gets the directory synchronization settings.

## EXAMPLES


## PARAMETERS

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
[Set-MsolDirSyncConfiguration](./Set-MsolDirSyncConfiguration.md)
