---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 692698D2-D070-449D-B112-1CEB30743A38
---

# Set-MsolServicePrincipal

## SYNOPSIS
Updates a service principal in Microsoft Azure Active Directory.

## SYNTAX

```
Set-MsolServicePrincipal [-ObjectId <Guid>] [-AppPrincipalId <Guid>] [-DisplayName <String>]
 [-ServicePrincipalNames <String[]>] [-AccountEnabled <Boolean>] [-Addresses <RedirectUri[]>]
 [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolServicePrincipal cmdlet updates a service principal in Microsoft Azure Active Directory.
It can be used to update the display name, enable/disable the service principal, trusted for delegation, the service principal names (SPNs) or the addresses.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
$AppId = (Get-MsolServicePrincipal -ServicePrincipalName "MyApp").AppPrincipalId
          Set-MsolServicePrincipal -AppPrincipalId $AppId -DisplayName "My Super Application" -ServicePrincipalNames @("MyApp/myapp.com", "MyApp/mysuperapp.com")
```

Description

-----------

This command updates properties on the specified service principal.
In this example, it specifies updates to the display name and the service principal names.
This will overwrite any previous settings.

### -------------------------- EXAMPLE 2 --------------------------
```
$a = @()
          $a = $a + (Get-MsolServicePrincipal -ServicePrincipalName "MyApp").Addresses
          $a = $a + (New-MsolServicePrincipalAddress -Value "myApp1.com")
          $a = $a + (New-MsolServicePrincipalAddress -Value "myApp2.com")
          Set-MsolServicePrincipal -AppPrincipalId $AppId -Addresses $a
```

Description

-----------

This command updates a service principal's associated addresses.
In this example, existing Addresses that were previously created ("myApp1.com", "myApp2.com") using the New-MsolServicePrincipalAddress helper command, are associated with the service principal.

## PARAMETERS

### -AccountEnabled
This property is reserved for future use.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Addresses
Specify the addresses list to update (and overwrite) the existing list with. 
If this is set to NULL, the existing property will not be updated. 
If this is set to an empty list, the existing Addresses will be cleared. 
Use the New-MsolServicePrincipalAddress cmdlet to help create the Addresses list object.

```yaml
Type: RedirectUri[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AppPrincipalId
The unique application identifier associated with the service principal to be updated.

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
The friendly name of the service principal.

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
The object ID associated with the service principal to be updated.

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

### -ServicePrincipalNames
Specify the service principal names (SPNs) list to update (and overwrite) the existing list with. 
If this is set to NULL, the existing property will not be updated. 
If this is set to an empty list, the existing SPNs will be cleared, except for the SPN containing the service principal's AppId value.
            An SPN must use one of the following formats "appName" or "appName/hostname" or be a valid URL.

```yaml
Type: String[]
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


