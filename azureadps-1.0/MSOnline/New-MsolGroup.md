---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 046485AB-D8CC-4DBB-9129-B987A91188CF
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-MsolGroup

## SYNOPSIS
Adds a new group to the Azure Active Directory.

## SYNTAX

```
New-MsolGroup [-DisplayName <String>] [-Description <String>] [-ManagedBy <String>] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-MsolGroup** cmdlet adds a new security group to Azure Active Directory.

## EXAMPLES

### Example 1: Create a security group
```
PS C:\> New-MsolGroup -DisplayName "MyGroup" -Description "My test group"
```

This command creates a security group called MyGroup.

## PARAMETERS

### -Description
Specifies a description of the group.

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

### -DisplayName
Specifies a display name of the group.

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

### -ManagedBy
Specifies the owner of the group.

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

### Microsoft.Online.Administration.Group
Will return the new group that was created.

## NOTES

## RELATED LINKS
[Get-MsolGroup](./Get-MsolGroup.md)

[Remove-MsolGroup](./Remove-MsolGroup.md)

[Set-MsolGroup](./Set-MsolGroup.md)
