---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D777B598-B7CC-445E-9F7A-4E21D79BBE39
---

# Remove-MsolContact

## SYNOPSIS
Removes a contact from Microsoft Azure Active Directory.

## SYNTAX

```
Remove-MsolContact -ObjectId <Guid> [-Force] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-MsolContact cmdlet is used to delete a contact from Microsoft Azure Active Directory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MsolContact -objectid <id> -force

          None
```

Description

-----------

This command removes a contact from the directory.

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
The unique ID of the contact to remove.

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


