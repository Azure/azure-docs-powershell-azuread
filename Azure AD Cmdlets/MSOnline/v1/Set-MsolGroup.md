---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 1D23EC9E-30E3-4B23-82E8-6B5C91F523A4
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
The Set-MsolGroup cmdlet is used to update the properties of a security group.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
$groupid = Get-MsolGroup -searchstring MyGroup
          Set-MsolGroup -objectid $groupId -Description "My Group"
```

Description

-----------

Updates the description for MyGroup.

## PARAMETERS

### -Description
The description of the group.

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
The display name of the group.

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
The owner of the group.

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
The ObjectId of the group to update.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


