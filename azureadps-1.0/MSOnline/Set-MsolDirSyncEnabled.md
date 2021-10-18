---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 2874711E-96F5-43E8-8D90-332C65A85FB5
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolDirSyncEnabled

## SYNOPSIS
Turns directory synchronization on or off for a company.

## SYNTAX

```
Set-MsolDirSyncEnabled -EnableDirSync <Boolean> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolDirSyncEnabled** cmdlet turns directory synchronization on or off for a company.

>**Important**: Once you have disabled dirsync through this cmdlet it may take 72 hours for deactivation to be completed. The time depends on the number of objects that are in your cloud service subscription account. **You cannot cancel the disable action**, it will need to complete before you can take any other action, including re-enabling of DirSync. If you choose to re-enable DirSync, a full synchronization of your synced objects will happen. This may take a considerable time depending on the number of objects in your Active Directory.

>Note: If you have disabled DirSync and then decide to re-enable DirSync, and if you had previously enabled the DirSync feature BlockCloudObjectTakeoverThroughHardMatch, OnPrem to cloud object takeover/update will be blocked for all objects which were mastered in Active Directory before. If this is the case and you want to resume syncing Active Directory mastered obejcts with Azure AD then you will need to set BlockCloudObjectTakeoverThroughHardMatch feature to false. You can read more about the DirSync features in [this article](https://docs.microsoft.com/powershell/module/msonline/set-msoldirsyncfeature?view=azureadps-1.0#example-3--block-cloud-object-takeover-through-hard-matching-for-the-tenant.md)


## EXAMPLES

### Example 1: Turn on directory synchronization
```
PS C:\> Set-MsolDirSyncEnabled -EnableDirsync $True
```

This command turns on directory synchronization for a company.

## PARAMETERS

### -EnableDirSync
Specifies whether to turn on directory synchronization on for your company.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
