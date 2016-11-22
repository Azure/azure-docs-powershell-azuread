---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADDeviceRegisteredUser

## SYNOPSIS
Add a user to a device.

## SYNTAX

```
Add-AzureADDeviceRegisteredUser -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### This example shows how to add a user as a registered user for a device
```
$User = get-azureaduser -top 1
$Device = Get-AzureADDevice -top 1
Add-AzureADDeviceRegisteredUser -ObjectId $Device.ObjectId -RefObjectId $User.ObjectId
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

### -RefObjectId
The unique identifier of the specific Azure Active Directory object that will be assigned as user

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

