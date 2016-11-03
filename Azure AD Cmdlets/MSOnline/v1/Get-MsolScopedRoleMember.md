---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 16B61372-E804-41E7-9B03-8752A76DD2CB
---

# Get-MsolScopedRoleMember

## SYNOPSIS
Retrieves the members of the specified role who are granted that role over an administrative unit.

## SYNTAX

### ListRoleScopedMembers__0 (Default)
```
Get-MsolScopedRoleMember [-AdministrativeUnitObjectId <Guid>] [-RoleObjectId <Guid>] [-MaxResults <Int32>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolScopedRoleMember [-AdministrativeUnitObjectId <Guid>] [-RoleObjectId <Guid>] [-All] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolScopedRoleMember cmdlet is used to the retrieve members of the specified role who are granted that role over an administrative unit.

## EXAMPLES

### --------------------------  Example 1  --------------------------
@{paragraph=PS C:\\\>}



```
$westcoastau = Get-MsolAdministrativeUnit -searchstring "West Coast"
          $uaadmin = Get-MsolRole -RoleName "User Account Administrator"
          Get-MsolScopedRoleMember -RoleObjectId $uaadmin.ObjectId -AdministrativeUnitObjectId $westcoastau.ObjectId
```

Description

-----------

This command will list all members of the "User Account Administrator" role that is scoped to the administrative unit "West Coast".

## PARAMETERS

### -RoleObjectId
The role whose scoped members should be returned.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUnitObjectId
The object ID of the administrative unit whose administrators should be returned.
Omit this parameter to find administrators for all administrative units.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
The maximum number of results returned for a search result.

```yaml
Type: Int32
Parameter Sets: ListRoleScopedMembers__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
The unique ID of the tenant to perform the operation on.
If this is not provided, then the value will default to the tenant of the current user.
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

### -All
If present then all results will be returned. 
Cannot be used with the MaxResults parameter.

```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.RoleScopedMember
For this cmdlet, each output object will include the following:
            DisplayName: The display name of the scoped role member.
            UserPrincipalName: The user principal name of the scoped role member.
            ObjectId: The unique ID of the scoped role member.

## NOTES

## RELATED LINKS


