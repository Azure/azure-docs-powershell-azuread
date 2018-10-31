---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 1D23EC9E-30E3-4B23-82E8-6B5C91F523A4
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolGroup

## SYNOPSIS
Updates a security group.

## SYNTAX

```
Set-MsolGroup [-ObjectId <Guid>] [-DisplayName <String>] [-Description <String>] [-ManagedBy <String>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolGroup** cmdlet updates the properties of a security group.

## EXAMPLES

### Example 1: Modify a group
```
PS C:\> $GroupId = Get-MsolGroup -SearchString "MyGroup"
PS C:\> Set-MsolGroup -ObjectId $GroupId -Description "My Group"
```

The first command gets the security group that matches the string MyGroup, and then stores it in the $GroupId variable.
The second command modifies the group in $GroupId.

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

### -ObjectId
Specifies the unique object ID of the group to update.

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

[Remove-MsolGroup](./Remove-MsolGroup.md)
