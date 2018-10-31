---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 66F7F0D7-A464-4E72-971F-73E3DFF04A70
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolDirSyncConfiguration

## SYNOPSIS
Modifies the directory synchronization settings.

## SYNTAX

```
Set-MsolDirSyncConfiguration -AccidentalDeletionThreshold <UInt32> [-Force] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolDirSyncConfiguration** cmdlet modifies the directory synchronization settings.

## EXAMPLES


## PARAMETERS

### -AccidentalDeletionThreshold
Specifies the accidental deletion threshold.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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
[Get-MsolDirSyncConfiguration](./Get-MsolDirSyncConfiguration.md)
