---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADObjectByObjectId

## SYNOPSIS
Retrieves the object(s) specified by the objectIds parameter 

## SYNTAX

```
Get-AzureADObjectByObjectId -ObjectIds <System.Collections.Generic.List`1[System.String]>
 [-Types <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves the object(s) specified by the objectIds parameter

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Get-AzureADObjectByObjectId -ObjectIds 2af3478a-27da-4837-a387-b22b3fb236a8, c4fdf87f-f68e-4859-8bcf-36579b66005e

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
c4fdf87f-f68e-4859-8bcf-36579b66005e 71715b24-8cdd-432b-a138-86e8ad179274 Woodgrove HR App

DeletionTimeStamp                   :
ObjectId                            : 2af3478a-27da-4837-a387-b22b3fb236a8
ObjectType                          : DeviceConfiguration
PublicIssuerCertificates            : {}
CloudPublicIssuerCertificates       : {}
RegistrationQuota                   : 20
MaximumRegistrationInactivityPeriod : 90
```

In this example two objects are retrieved (a DeviceConfiguration object and an Application object) as specified by the value of the ObjectIds parameter

## PARAMETERS

### -ObjectIds
One or more object ID's, separated by commas, for which the objects are retrieved

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Types
Specifies the type of objects that the cmdlet returns

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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

