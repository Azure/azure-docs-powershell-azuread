---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0A3B58FA-9320-4E23-90AA-A75842492AC9
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolUserLicense

## SYNOPSIS
Updates the license assignment for a user.

## SYNTAX

### SetUserLicenses__0 (Default)
```
Set-MsolUserLicense -ObjectId <Guid> [-LicenseOptions <LicenseOption[]>] [-AddLicenses <String[]>]
 [-RemoveLicenses <String[]>] [-TenantId <Guid>] [<CommonParameters>]
```

### SetUserLicensesByUpn__0
```
Set-MsolUserLicense [-LicenseOptions <LicenseOption[]>] -UserPrincipalName <String> [-AddLicenses <String[]>]
 [-RemoveLicenses <String[]>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolUserLicense** cmdlet updates the license assignment for a user.
This can include adding a new license, removing a license, updating the license options, or any combination of these actions.

## EXAMPLES

### Example 1: Add a license to a user
```
PS C:\> Set-MsolUserLicense -UserPrincipalName "davidchew@contoso.com" -AddLicenses "Contoso:ENTERPRISEPACK"
```

This command adds the Office 365 for Enterprises license to the user.

### Example 2: Remove a license from a user
```
PS C:\> Set-MsolUserLicense -UserPrincipalName "davidchew@contoso.com" -RemoveLicenses "contoso:ENTERPRISEPACK"
```

This command removes the Office 365 for Enterprises license from the user.
This may result in the user's data being removed from each service.

### Example 3: Replace one license with another
```
PS C:\> Set-MsolUserLicense -UserPrincipalName "davidchew@contoso.com" -AddLicenses "contoso:DESKLESS" -RemoveLicenses "contoso:ENTERPRISEPACK"
```

This command replaces the Office 365 for Enterprises license with an Office 365 Deskless license.
These changes are made in one single operation.
Therefore, the user does not end up in an intermediate state where the Office 365 for Enterprises license is removed without Office 365 Deskless being added.

## PARAMETERS

### -AddLicenses
Specifies an array of licenses to assign to the user.

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

### -LicenseOptions
Specifies an array of license- or SKU-specific settings.
Used to disable individual services when assigning a license.

```yaml
Type: LicenseOption[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the user for which to update licenses.

```yaml
Type: Guid
Parameter Sets: SetUserLicenses__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemoveLicenses
Specifies an array of licenses to remove from the user.

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

### -UserPrincipalName
Specifies the user principal name of the user to update.

```yaml
Type: String
Parameter Sets: SetUserLicensesByUpn__0
Aliases:

Required: True
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
[Set-MsolUserPassword](./Set-MsolUserPassword.md)

[Set-MsolUserPrincipalName](./Set-MsolUserPrincipalName.md)
