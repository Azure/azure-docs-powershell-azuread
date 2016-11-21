---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Add-AzureADDeviceRegisteredOwner

## SYNOPSIS
Add an owner to a device

## SYNTAX

```
Add-AzureADDeviceRegisteredOwner -ObjectId <String> -RefObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Add a user as an owner of a device
```
$User = get-azureaduser -top 1
$Device = Get-AzureADDevice -top 1
Add-AzureADDeviceRegisteredOwner -ObjectId $Device.ObjectId -RefObjectId $User.ObjectId
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
The unique identifier of the specific Azure Active Directory object that will be assigned as owner

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

