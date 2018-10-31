---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: E748C8B0-B3F1-4BF5-8296-C2C2E8C54FB0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Remove-MsolGroup

## SYNOPSIS
Removes a group from Azure Active Directory.

## SYNTAX

```
Remove-MsolGroup -ObjectId <Guid> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MsolGroup cmdlet** deletes a group from Azure Active Directory.

## EXAMPLES

### Example 1: Remove a security group
```
PS C:\> $GroupId = Get-MsolGroup -SearchString "MyGroup"
PS C:\> Remove-MsolGroup -objectid $GroupId
```

The first command gets the security group that matches the string MyGroup, and then stores it in the $GroupId variable.
The second command removes the group in $GroupId.

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
Specifies the unique object ID of the group to remove.

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
[Get-MsolGroup](./Get-MsolGroup.md)

[New-MsolGroup](./New-MsolGroup.md)

[Set-MsolGroup](./Set-MsolGroup.md)
