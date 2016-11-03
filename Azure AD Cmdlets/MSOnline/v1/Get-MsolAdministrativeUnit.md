---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 87C2C236-9B82-45D1-BD68-6B118033064C
---

# Get-MsolAdministrativeUnit

## SYNOPSIS
Retrieves administrative units from Azure AD.

## SYNTAX

### ListAdministrativeUnits__0 (Default)
```
Get-MsolAdministrativeUnit [-UserObjectId <Guid>] [-UserPrincipalName <String>] [-SearchString <String>]
 [-MaxResults <Int32>] [-TenantId <Guid>] [<CommonParameters>]
```

### GetAdministrativeUnit__0
```
Get-MsolAdministrativeUnit -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolAdministrativeUnit [-UserObjectId <Guid>] [-UserPrincipalName <String>] [-SearchString <String>] [-All]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolAdministrativeUnit cmdlet is used to retrieve administrative units from Azure AD.

## EXAMPLES

### --------------------------  Example 1  --------------------------
@{paragraph=PS C:\\\>}



```
Get-MsolAdministrativeUnit
```

Description

-----------

This command gets all of the administrative units in the tenant of the currently authenticated user.

### --------------------------  Example 2  --------------------------
@{paragraph=PS C:\\\>}



```
Get-MsolAdministrativeUnit -SearchString "West Coast"
```

Description

-----------

This command retrieves the administrative unit called "West Coast".

### --------------------------  Example 3  --------------------------
@{paragraph=PS C:\\\>}



```
Get-MsolAdministrativeUnit -UserPrincipalName "user1@contoso.com"
```

Description

-----------

This command gets the administrative units in which user1@contoso.com is a member.

## PARAMETERS

### -UserObjectId
The unique ID of a user.
If provided, only administrative units that this user belongs to will be returned.

```yaml
Type: Guid
Parameter Sets: ListAdministrativeUnits__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
The user principal name of a user.
If provided, only administrative units that this user belongs to will be returned.

```yaml
Type: String
Parameter Sets: ListAdministrativeUnits__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
The string to search on.
Only administrative units with a display name starting with this string will be returned.

```yaml
Type: String
Parameter Sets: ListAdministrativeUnits__0, All__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
The maximum number of results returned.

```yaml
Type: Int32
Parameter Sets: ListAdministrativeUnits__0
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

### -ObjectId
The unique ID of the administrative unit to retrieve.

```yaml
Type: Guid
Parameter Sets: GetAdministrativeUnit__0
Aliases: 

Required: True
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

## NOTES

## RELATED LINKS


