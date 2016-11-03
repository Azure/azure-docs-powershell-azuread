---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 287EDFB6-E2D4-417A-B8B2-29D6EFD9F1E7
---

# Set-MsolAdministrativeUnit

## SYNOPSIS
Updates the properties of an administrative unit.

## SYNTAX

```
Set-MsolAdministrativeUnit [-ObjectId <Guid>] [-DisplayName <String>] [-Description <String>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolAdministrativeUnit cmdlet is used to update the properties of an administrative unit.

## EXAMPLES

### --------------------------  Example 1  --------------------------
@{paragraph=PS C:\\\>}



```
$au = Get-MsolAdministrativeUnit -searchstring "West Coast"
          Set-MsolAdministrativeUnit -Description "West Coast region" -ObjectID $au.ObjectId
```

Description

-----------

This command first locates the administrative unit with the name "West Coast", then assigns it a description value of "West Coast region".

## PARAMETERS

### -ObjectId
The unique ID of the administrative unit to update.

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

### -DisplayName
The display name of the administrative unit.

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

### -Description
The description of the administrative unit.

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


