﻿---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 728230E1-6984-49F8-B153-B73A7724EF5A
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Redo-MsolProvisionUser

## SYNOPSIS
Retries the provisioning of a user object in Azure Active Directory.

## SYNTAX

```
Redo-MsolProvisionUser -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Redo-MsolProvisionUser** cmdlet retries the provisioning of a user object in Azure Active Directory when a previous attempt to create the user object resulted in a validation error.

## PARAMETERS

### -ObjectId
Specifies the unique object ID associated with the user object on which to retry provisioning.

```yaml
Type: Guid
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

## NOTES

## RELATED LINKS
[Redo-MsolProvisionContact](./Redo-MsolProvisionContact.md)

[Redo-MsolProvisionGroup](./Redo-MsolProvisionGroup.md)
