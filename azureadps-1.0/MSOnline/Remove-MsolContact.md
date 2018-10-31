---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D777B598-B7CC-445E-9F7A-4E21D79BBE39
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolContact

## SYNOPSIS
Removes a contact from Azure Active Directory.

## SYNTAX

```
Remove-MsolContact -ObjectId <Guid> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolContact** cmdlet deletes a contact from Azure Active Directory.

## EXAMPLES

### Example 1: Remove a contact
```
PS C:\> Remove-MsolContact -ObjectId 40c4ca1a-4e15-40ad-b0bd-abeca4bcafcd -Force
```

This command removes a contact from the Azure Active Directory.

## PARAMETERS

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

### -ObjectId
Specifies the unique ID of the contact to remove.

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
[Get-MsolContact](./Get-MsolContact.md)
