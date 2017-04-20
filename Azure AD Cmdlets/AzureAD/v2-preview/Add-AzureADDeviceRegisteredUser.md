---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 2CFAF4EB-D639-4B11-8A1F-6D011BBE4ACA
online version: 
schema: 2.0.0
---

# Add-AzureADDeviceRegisteredUser

## SYNOPSIS
Adds a registered user for a device.

## SYNTAX

```
Add-AzureADDeviceRegisteredUser -ObjectId <String> -RefObjectId <String> [<CommonParameters>]
```

## DESCRIPTION
The **Add-AzureADDeviceRegisteredUser** cmdlet adds a registered user for an Azure Active Directory device.

## EXAMPLES

### Example 1: Add a user as a registered user
```
PS C:\> $User = Get-AzureADUser -Top 1
PS C:\> $Device = Get-AzureADDevice -Top 1
PS C:\> Add-AzureADDeviceRegisteredUser -ObjectId $Device.ObjectId -RefObjectId $User.ObjectId
```

The first command gets a user by using the [Get-AzureADUser](./Get-AzureADUser.md) cmdlet, and then stores it in the $User variable. 

The second command gets a device by using the [Get-AzureADDevice](./Get-AzureADDevice.md) cmdlet, and then stores it in the $Device variable.

The final command adds the user in $User as the registered user for the device in $Device. 
Both parameters use the **ObjectId** property of specified object. 

## PARAMETERS

### -ObjectId
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

### -RefObjectId
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDevice](./Get-AzureADDevice.md)

[Get-AzureADDeviceRegisteredUser](./Get-AzureADDeviceRegisteredUser.md)

[Get-AzureADUser](./Get-AzureADUser.md)

[Remove-AzureADDeviceRegisteredUser](./Remove-AzureADDeviceRegisteredUser.md)
