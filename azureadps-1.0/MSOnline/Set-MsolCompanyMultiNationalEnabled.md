---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 5AA049F5-BA10-437E-BE0C-E7E66CA795E9
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolCompanyMultiNationalEnabled

## SYNOPSIS
Enables the multinational feature for a service type for a company with Azure Active Directory.

## SYNTAX

```
Set-MsolCompanyMultiNationalEnabled -ServiceType <String> -Enable <Boolean> [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolCompanyMultiNationalEnabled** cmdlet attempts to enable the multinational feature for a service type for a company in v1.
This cmdlet returns an error with the failure reason if the multinational feature for a service type cannot be enabled for a company.

Disabling or opting out from the multinational feature for a service type is not supported in v1.


## EXAMPLES

### Example 1: Attempt to enable the multinational feature for a service
```
PS C:\> Set-MsolCompanyMultiNationalEnabled -ServiceType "MicrosoftCommunicationsOnline" -Enable $True
```
This command attempts to enable the multinational feature for the MicrosoftCommunicationsOnline service type for a company.
The Microsoft communications online service type is also known as Skype for Business.

## PARAMETERS

### -ServiceType
Specifies the service type for which to enable the multinational feature.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Enable
Indicates whether to enable or disable the multinational feature for a service type for a company.

```yaml
Type: Boolean
Parameter Sets: (All)
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

## NOTES

## RELATED LINKS
