---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 843652E4-266F-4F05-A1C5-8E8EBC86241D
---

# Get-MsolAccountSku

## SYNOPSIS
Retrieves all the SKUs for a company.

## SYNTAX

```
Get-MsolAccountSku [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-MsolAccountSku will return all the SKUs that the company owns.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolAccountSku

          Returns a list of SKUs.
```

Description

-----------

This command returns a list of SKUs.

## PARAMETERS

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

### Microsoft.Online.Administration.AccountSKU
Each AccountSKU returned will include the following information:

            AccountName: The name of the account this SKU belongs to.

            AccountObjectId: The unique ID of the account this SKU belongs to.

            AccountSkuId: The unique string ID of the account/SKU combination.
This value should be used when assigning or updating licenses.

            ActiveUnits: The number of active licenses.

            ConsumedUnits: The number of licenses consumed.

            ServiceStatus: The provisioning status of individual services belonging to this SKU.

            SkuId: The unique ID for the SKU.

            SkuPartNumber: The partner number of this SKU.

            SubscriptionIds: A list of all subscriptions associated with this SKU.
For the purposes of assigning licenses, all subscriptions with the same SKU will be grouped into a single license pool.

            SuspendedUnits: The number of suspended licenses.
These licenses are not available for assignment.

            TargetClass: The target class of this SKU.
Only SKUs with target class=user are assignable.

            WarningUnits: The number of warning units.

## NOTES

## RELATED LINKS


