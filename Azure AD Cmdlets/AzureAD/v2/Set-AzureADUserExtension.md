---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADUserExtension

## SYNOPSIS

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Set-AzureADUserExtension -ObjectId <String> -ExtensionName <String> -ExtensionValue <String>
```

### UNNAMED_PARAMETER_SET_2
```
Set-AzureADUserExtension -ObjectId <String> -ExtensionNameValues <Dictionary`2[String]>
```

## DESCRIPTION

## EXAMPLES

### Set the value of an extension attribute for a user
```
$User = Get-AzureADUser -top 1
Set-AzureADUserExtension -ObjectId $User.ObjectId -ExtensionName extension_e5e29b8a85d941eab8d12162bd004528_extensionAttribute8 -ExtensionValue "New Value"
```

This cmdlet sets the value of the extension attriute with name extension_e5e29b8a85d941eab8d12162bd004528_extensionAttribute8 to the value "New Value".


Note that extension attribute names can be found by using the Get-AzureAdExtensionProperty cmdlet

## PARAMETERS

### -ObjectId
@{Text=}

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

### -ExtensionName
@{Text=}

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionValue
@{Text=}

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionNameValues
@{Text=}

```yaml
Type: Dictionary`2[String]
Parameter Sets: UNNAMED_PARAMETER_SET_2
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

