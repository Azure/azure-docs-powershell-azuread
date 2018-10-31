---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0633C5AB-EA9A-4B55-959D-26611F16AB43
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolSubscription

## SYNOPSIS
Gets subscriptions.

## SYNTAX

### ListSubscriptions__0 (Default)
```
Get-MsolSubscription [-TenantId <Guid>] [<CommonParameters>]
```

### GetSubscription__0
```
Get-MsolSubscription -SubscriptionId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolSubscription** cmdlet gets all the subscriptions that the company has purchased.
When assigning licenses to users, the [Get-MsolAccountSku](./Get-MsolAccountSku.md) cmdlet should be used instead.

## EXAMPLES

### Example 1: Gets a list of company subscriptions
```
PS C:\> Get-MsolSubscription
```

This command gets a list of company subscriptions.
For license assignment,  the [Get-MsolAccountSku](./Get-MsolAccountSku.md) cmdlet should be used instead.

## PARAMETERS

### -SubscriptionId
Specifies the unique object ID of the subscription to retrieve.

```yaml
Type: Guid
Parameter Sets: GetSubscription__0
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Subscription
This cmdlet returns subscription objects that contain the following information:

* DateCreated. The date that this subscription was created.

* NextLifecycleDate. The date of the next lifecycle event for this subscription.

* ObjectId. The unique ID of this subscription.

* OcpSubscriptionId. The ID of this subscription in the commerce system.

* ServiceStatus. The provisioning status of each service associated with this subscription.

* SkuId. The object ID of the SKU associated with this subscription.

* SkuPartNumber. The SKU associated with this subscription.

* Status. The status of this subscription (Enabled, Expired, or Suspended).

* TotalLicenses. The number of seats included in this subscription.

## NOTES

## RELATED LINKS
[Get-MsolAccountSku](./Get-MsolAccountSku.md)
