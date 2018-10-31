---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 843652E4-266F-4F05-A1C5-8E8EBC86241D
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolAccountSku

## SYNOPSIS
Returns all the SKUs for a company.

## SYNTAX

```
Get-MsolAccountSku [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolAccountSku** cmdlet returns all the SKUs that the company owns.

## EXAMPLES

### Example 1: Get the company SKUs
```
PS C:\> Get-MsolAccountSku
```

This command returns a list of SKUs.

### Example 2: Get available services
```
PS C:\> Get-MsolAccountSku | select -ExpandProperty ServiceStatus
```

This command returns a list of available services. This is very useful when you work with **New-MsolLicenseOptions** cmdlet and want to disable certain services for specific users. For more information, see: 
* [New-MsolLicenseOptions](https://docs.microsoft.com/en-us/powershell/module/msonline/new-msollicenseoptions?view=azureadps-1.0 "New-MsolLicenseOptions")  
* [View licenses and services with Office 365 PowerShell](https://technet.microsoft.com/en-us/library/dn771773.aspx?f=255&MSPPError=-2147217396)

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.AccountSKU
The cmdlet returns AccountSKU objects that contain the following information:

* AccountName. The name of the account this SKU belongs to.

* AccountObjectId. The unique ID of the account this SKU belongs to.

* AccountSkuId. The unique string ID of the account/SKU combination.
This value should be used when assigning or updating licenses.

* ActiveUnits. The number of active licenses.

* ConsumedUnits. The number of licenses consumed.

* ServiceStatus. The provisioning status of individual services belonging to this SKU.

* SkuId. The unique ID for the SKU.

* SkuPartNumber. The partner number of this SKU.

* SubscriptionIds. A list of all subscriptions associated with this SKU.
For the purposes of assigning licenses, all subscriptions with the same SKU will be grouped into a single license pool.

* SuspendedUnits. The number of suspended licenses.
These licenses are not available for assignment.

* TargetClass. The target class of this SKU.
Only SKUs with target class=user are assignable.

* WarningUnits. The number of warning units.

## NOTES

## RELATED LINKS  
[View licenses and services with Office 365 PowerShell](https://technet.microsoft.com/en-us/library/dn771773.aspx?f=255&MSPPError=-2147217396)
