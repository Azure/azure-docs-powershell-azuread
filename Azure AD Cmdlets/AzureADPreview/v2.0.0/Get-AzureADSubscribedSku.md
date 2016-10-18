---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 0E1A27BF-2CD9-43CD-851D-D1F09484CDE3
---

# Get-AzureADSubscribedSku

## SYNOPSIS
Retrieves a list of subscribed skus (subscriptions) to Microsoft services.

## SYNTAX

```
Get-AzureADSubscribedSku [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\>Get-AzureADSubscribedSku
```

Output:

ObjectId                                                                  SkuPartNumber         PrepaidUnits                                                             ConsumedUnits
--------                                                                  -------------         ------------                                                             -------------
85b5ff1e-0402-400c-9e3c-0f9e965325d1_078d2b04-f1bd-4111-bbd4-b4b1b354cef4 AAD_PREMIUM           class LicenseUnitsDetail {... 
6
85b5ff1e-0402-400c-9e3c-0f9e965325d1_f245ecc8-75af-4f8e-b61f-27d8114de5f3 O365_BUSINESS_PREMIUM class LicenseUnitsDetail {... 
24

## PARAMETERS

### -InformationAction
@{Text=}```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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


