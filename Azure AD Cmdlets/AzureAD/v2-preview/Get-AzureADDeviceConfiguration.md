---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADDeviceConfiguration

## SYNOPSIS
This cmdlet retrieves the device configuration object

## SYNTAX

```
Get-AzureADDeviceConfiguration [<CommonParameters>]
```

## DESCRIPTION
This cmdlet retrieves the device configuration object

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADDeviceConfiguration | fl


DeletionTimeStamp                   :
ObjectId                            : 2af3478a-27da-4837-a387-b22b3fb236a8
ObjectType                          : DeviceConfiguration
PublicIssuerCertificates            : {}
CloudPublicIssuerCertificates       : {}
RegistrationQuota                   : 20
MaximumRegistrationInactivityPeriod : 90
```

This example shows the formatted list for the device configuration record that is retrieved by the cmdlet

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

