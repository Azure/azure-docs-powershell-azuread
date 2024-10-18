---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Get-AzureADUserLicenseDetail

## SYNOPSIS
Retrieves license details for a user

## SYNTAX

```
Get-AzureADUserLicenseDetail -ObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
THis cmdlet retrieves license details for a user

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADUserLicenseDetail -ObjectId aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb

ObjectId                                    ServicePlans
--------                                    ------------
Hv-1hQIEDECePA-ellMl0cjsRfKvdY5Pth8n2BFN5fM {class ServicePlanInfo {...
Hv-1hQIEDECePA-ellMl0QQrjQe98RFBu9S0sbNUzvQ {class ServicePlanInfo {...
```

This example retrieves the license details of the user specified through the ObjectId parameter

## PARAMETERS

### -ObjectId
The object ID of the user for which the license details are retrieved

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
