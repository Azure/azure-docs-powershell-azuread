---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 8D9F4A29-671A-468A-9B20-B985DF1B4EC2
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-MsolLicenseOptions

## SYNOPSIS
Creates a License Options object.

## SYNTAX

```
New-MsolLicenseOptions -AccountSkuId <String>
 [-DisabledPlans <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MsolLicenseOptions** cmdlet creates a License Options object.
This cmdlet disables specific service plans when assigning a user a license using the [Set-MsolUserLicense](./Set-MsolUserLicense.md) cmdlet.

## EXAMPLES

### Example 1: Create license options object
```
PS C:\> New-MsolLicenseOptions -AccountSkuId Contoso:BPOS_STANDARD -DisabledPlans EXCHANGE_STANDARD
```

This command creates a license options object.
This object can be used for the license options parameter in the [New-MsolUser](./New-MsolUser.md) or [Set-MsolUserLicense](./Set-MsolUserLicense.md) cmdlets.

## PARAMETERS

### -AccountSkuId
Specifies the license, or account SKU ID, for these options.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisabledPlans
Specifies a list of service plans to disable when assigning this license to the user.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
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

[New-MsolUser](./New-MsolUser.md)

[Set-MsolUserLicense](./Set-MsolUserLicense.md)
