---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 13ECD260-8B3D-4D47-9109-86DDFC235C92
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolApplicationPassword

## SYNOPSIS
Removes a password for an application.

## SYNTAX

```
Remove-MsolApplicationPassword -UserPrincipalName <String> -PasswordId <String> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolApplicationPassword** cmdlet removes a password for an application.


## EXAMPLES


## PARAMETERS

### -PasswordId
Specifies the ID of the password to remove.

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

### -UserPrincipalName
Specifies the user principal name for which to remove a password.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
