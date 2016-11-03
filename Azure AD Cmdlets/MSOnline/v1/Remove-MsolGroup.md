---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: E748C8B0-B3F1-4BF5-8296-C2C2E8C54FB0
---

# Remove-MsolGroup

## SYNOPSIS
Removes a group from Microsoft Azure Active Directory.

## SYNTAX

```
Remove-MsolGroup -ObjectId <Guid> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolGroup cmdlet is used to delete a group from Microsoft Azure Active Directory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
$groupId = Get-MsolGroup -searchString "MyGroup"
          Remove-MsolGroup -objectid $groupId
```

Description

-----------

Will remove the group "MyGroup" from the directory.

## PARAMETERS

### -Force
Used to bypass onscreen confirmation.

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
The unique ID of the group to remove.

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


