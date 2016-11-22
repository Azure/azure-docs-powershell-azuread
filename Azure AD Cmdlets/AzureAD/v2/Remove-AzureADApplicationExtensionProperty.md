---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADApplicationExtensionProperty

## SYNOPSIS
Delete an application extension property.

## SYNTAX

```
Remove-AzureADApplicationExtensionProperty -ObjectId <String> -ExtensionPropertyId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove an application extension from the directory
```
Remove-AzureADApplicationExtensionProperty -ObjectId 3ddd22e7-a150-4bb3-b100-e410dea1cb84 -ExtensionPropertyId 344ed560-f8e7-410e-ab9f-c79df5c36
```

## PARAMETERS

### -ObjectId
The unique idenfier of an application in Azure Active Directory

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

### -ExtensionPropertyId
The unique identifier of the extension property

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

