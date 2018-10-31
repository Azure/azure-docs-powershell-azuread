---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: ACEA9C06-7619-4EAE-967D-280F982ECE7A
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# New-MsolServicePrincipalAddresses

## SYNOPSIS
Creates a service principal address.

## SYNTAX

```
New-MsolServicePrincipalAddresses -Address <String> [-AddressType <AddressType>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MsolServicePrincipalAddresses** cmdlet creates a service principal address.

## PARAMETERS

### -Address
Specifies an address to be used by an application.

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

### -AddressType
Specifies the type of address to create.
Valid values are:
* Reply
* Realm
* Error
* Other
* SamlMetadata
* SamlLogout

```yaml
Type: AddressType
Parameter Sets: (All)
Aliases:
Accepted values: Reply, Realm, Error, Other, SamlMetadata, SamlLogout

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
