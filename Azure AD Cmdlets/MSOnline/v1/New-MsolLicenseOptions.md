---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 8D9F4A29-671A-468A-9B20-B985DF1B4EC2
---

# New-MsolLicenseOptions

## SYNOPSIS
Creates a new License Options object.
This object is used when assigning licenses through Add-MSOLUser and Set-MsolUserLicense cmdlets.

## SYNTAX

```
New-MsolLicenseOptions -AccountSkuId <String>
 [-DisabledPlans <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
The New-MsolLicenseOptions cmdlet creates a new License Options object.
This cmdlet disables specific service plans when assigning a user a license using the Add-MsolUser and Set-MsolUserLicense cmdlets.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
New-MsolLicenseOption -AccountSkuId Contoso:BPOS_STANDARD -DisabledPlans EXCHANGE_STANDARD

          Returns a License Option object.
```

Description

-----------

This command creates a license options object. 
This can be used for the license options parameter in New-MsolUser or Set-MsolUserLicense.

## PARAMETERS

### -AccountSkuId
The license (AccountSkuID) for these options.

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
A list of service plans to disable when assigning this license to the user.

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


