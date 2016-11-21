---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADDeviceRegisteredUser

## SYNOPSIS
Removes a user from a device.

## SYNTAX

```
Remove-AzureADDeviceRegisteredUser -ObjectId <String> -UserId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove a registered user from a device
```
$Device = Get-AzureADDevice -top 1
$User = Get-AzureADDeviceRegisteredUser -ObjectId $Device.ObjectId
Remove-AzureADDeviceRegisteredUser -ObjectId $device.ObjectId -UserId $user.ObjectId
```

## PARAMETERS

### -ObjectId
The unique identifier of the device

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -UserId
The unique identifier of the user

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

